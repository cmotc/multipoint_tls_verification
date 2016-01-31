# multipoint_tls_verification
A script which attempts to increase how much trust one can have in an unsigned TLS certificate by attempting to collect them via Tor and from other alternative sources.

          ###===============---------------------------------===============###
          ##   Multipoint TLS Certificate Checker:                           ##
          #            Detect possible MITM attacks by obtaining TLS certs    #
          ##     via Tor from multiple exit nodes.                           ##
          ###===============---------------------------------===============###

          Description: This program retrieves the TLS certificate belonging to
          to the URL it is passed from a group of up to 5 different Tor exit
          nodes in order to detect differences between them(Such as those that
          might imply a Man-In-The-Middle Attack directed at a certain
          geograpic area. It currently DOES NOT protect against MITM attacks
          that specifically target traffic coming out of Tor exit nodes, but it
          may soon by adding support for querying convergence.io notaries and
          namecoin resolvers as well. Use with great caution and read the code!

            usage:
                -u The URL to test.
                -s The number of different Tor exit nodes to retrieve the cert
                    through.
                -v Verbose Mode(Inactive.)
                -h Displays this help message.