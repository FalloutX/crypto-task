## grunt-contrib-crypt

Grunt task to encrypt and decrypt files

## Usage

Encrypt files :

    $ grunt encrypt [--key mysecret]

Decrypt files :

    $ grunt decrypt [--key mysecret]

## Configuration

Put this in your grunt config :

    crypt:{
      files:[                                   // files to process
        {
          dir:'demo',                           // root dir of files to encrypt / decrypt
          include:'**/*.js',                    // pattern to include files
          encryptedExtension:'.encrypted'       // extension used for encrypted files
        }
      ],
      options:{
        key:grunt.cli.options.key || 'somekey'  // key used to encrypt / decrypt
                                                // for security purpose, prefer to pass it through command line arguments
      }
    }

Same 'crypt' config object is used to encrypt and decrypt files.

Enjoy !