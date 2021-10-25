# DependencyInjection

* Избавляемся от создания объекта класса `new MusicPlayer(music)` `<bean id="musicPlayer"
          class="ru.solomakhin.spring.MusicPlayer">
        <constructor-arg ref="musicBean"/>
    </bean>` - создаем бин, в котором указываем в теге `constructor-arg` аргументом `ref` id бина.
    
* В проекте вместо `Music music = context.getBean("musicBean", Music.class);` и `MusicPlayer musicPlayer = new MusicPlayer(music);` теперь достаточно `MusicPlayer musicPlayer = context.getBean("musicPlayer", MusicPlayer.class);
`
