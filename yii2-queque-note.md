yii2-queque-note
========================
There are note for  yii2-queue

config
------------

  ```
    ......
    'bootstrap' => [
        'log',
        'queue', // The component registers own console commands
    ],
    'components' => [
        'queue' => [
            'class' => \yii\queue\db\Queue::class,
            'as log' => \yii\queue\LogBehavior::class,
            // Other driver options
            'db' => 'db', // DB connection component or its config
            'tableName' => '{{%queue}}', // Table name
            'channel' => 'ingestion', // Queue channel key
            'mutex' => \yii\mutex\FileMutex::class,// The program will be wrong,if you not set it.
        ],
        ....
     ]

  ```
