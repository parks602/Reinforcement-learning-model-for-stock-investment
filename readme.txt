##########################################################################################################
## Reinforcement learning model for stock investment.                                                   ##
## Made by : PKW. KOAST                                                                                 ##
## Source of this code : https://github.com/quantylab/rltrader                                          ##
## Version : 0.0.1                                                                                      ##
## Last touch-up date : 2020-01-26                                                                      ##
##########################################################################################################


################################################################################################
2020-01-26
* Add pytorch gpu from the existing code

1. RUN : python main.py

       options : --stock_code
                 --ver : data form [v1, v2, v3, v4]
                 --rl_method : Reinforcement learning method choice [*dqn, pg(Policy Gradient), ac(Actor-Critic), a2c]
                         @@When using the a3c method, stock_code is must be multiple.
                 --net : Type of neral network [*dnn, cnn, lstm]
                         @@When using the cnn model or the lstm model, the 'num_stpes' factor is essential.
                 --lr *0.001
                 --start_epsilon *1
                 --discount_factor *0.9
                 --balance *10000000
                 --num_epoches *100
                 --backend [*pytorch, tensorflow, plaidml]
                 --output_name *In utils.py get_time_str() method
                 --value_network_name
                 --balance_network_name
                 --reuse_model
                 --learning
                 --start_date
                 --end_date

An example of an execution command : python main.py --stock_code 005930 --rl_method dqn --net dnn --learning --num_epoches 100 --lr 0.001 --start_epsilon 1 --discount_factor 0.9
