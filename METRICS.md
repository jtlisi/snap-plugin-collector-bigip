<!-- http://www.apache.org/licenses/LICENSE-2.0.txt

Copyright 2017 jtlisi

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License. -->
# snap plugin collector - BigIp

## Collected Metrics
This plugin has the ability to gather the following metrics:

a) **BigIp Node Metrics**

The prefix of metric's namespace is `/jtlisi/bigip/node/<partition>/<node>`

Namespace                                         | Data Type
--------------------------------------------------|-------------
/jtlisi/bigip/node/*/*/cur_sessions              | conn
/jtlisi/bigip/node/*/*/serverside_bytes_in       | B
/jtlisi/bigip/node/*/*/serverside_bytes_out      | B
/jtlisi/bigip/node/*/*/serverside_cur_conns      | conn
/jtlisi/bigip/node/*/*/serverside_max_conns      | conn
/jtlisi/bigip/node/*/*/serverside_pkts_in        | pckt
/jtlisi/bigip/node/*/*/serverside_pkts_out       | pckt
/jtlisi/bigip/node/*/*/serverside_tot_conns      | conn
/jtlisi/bigip/node/*/*/status_availability_state | availability
/jtlisi/bigip/node/*/*/tot_requests              | req

b) **BigIp Pool Metrics**

The prefix of metric's namespace is `/jtlisi/bigip/pool/<partition>/<pool>`

Namespace                                         | Data Type
--------------------------------------------------|----------
/jtlisi/bigip/pool/*/*/active_member_cnt         | counter
/jtlisi/bigip/pool/*/*/connq_age_edm             | s
/jtlisi/bigip/pool/*/*/connq_age_ema             | s
/jtlisi/bigip/pool/*/*/connq_age_head            | s
/jtlisi/bigip/pool/*/*/connq_age_max             | s
/jtlisi/bigip/pool/*/*/connq_all_age_edm         | s
/jtlisi/bigip/pool/*/*/connq_all_age_ema         | s
/jtlisi/bigip/pool/*/*/connq_all_age_head        | s
/jtlisi/bigip/pool/*/*/connq_all_age_max         | s
/jtlisi/bigip/pool/*/*/connq_all_depth           | conn
/jtlisi/bigip/pool/*/*/connq_all_serviced        | conn
/jtlisi/bigip/pool/*/*/connq_depth               | s
/jtlisi/bigip/pool/*/*/connq_serviced            | conn
/jtlisi/bigip/pool/*/*/cur_sessions              | conn
/jtlisi/bigip/pool/*/*/min_active_members        | counter
/jtlisi/bigip/pool/*/*/serverside_bytes_in       | B
/jtlisi/bigip/pool/*/*/serverside_bytes_out      | B
/jtlisi/bigip/pool/*/*/serverside_cur_conns      | conn
/jtlisi/bigip/pool/*/*/serverside_max_conns      | conn
/jtlisi/bigip/pool/*/*/serverside_pkts_in        | pckt
/jtlisi/bigip/pool/*/*/serverside_pkts_out       | pckt
/jtlisi/bigip/pool/*/*/serverside_tot_conns      | conn
/jtlisi/bigip/pool/*/*/status_availability_state | bool
/jtlisi/bigip/pool/*/*/tot_requests              | req

c) **BigIp Rule Metrics**

The prefix of metric's namespace is `/jtlisi/bigip/rule/<partition>/<rule>/<event>/`

Namespace                                  | Data Type
-------------------------------------------|----------
/jtlisi/bigip/rule/*/*/*/aborts           | event
/jtlisi/bigip/rule/*/*/*/avg_cycles       | event
/jtlisi/bigip/rule/*/*/*/failures         | event
/jtlisi/bigip/rule/*/*/*/max_cycles       | event
/jtlisi/bigip/rule/*/*/*/min_cycles       | event
/jtlisi/bigip/rule/*/*/*/priority         | event
/jtlisi/bigip/rule/*/*/*/total_executions | event


d) **BigIp VS Metrics**

The prefix of metric's namespace is `/jtlisi/bigip/rule/<partition>/<rule>/<event>/`

Namespace                                            | Data Type
-----------------------------------------------------|-------------
/jtlisi/bigip/vs/*/*/clientside_bytes_in            | B
/jtlisi/bigip/vs/*/*/clientside_bytes_out           | B
/jtlisi/bigip/vs/*/*/clientside_cur_conns           | conn
/jtlisi/bigip/vs/*/*/clientside_evicted_conns       | conn
/jtlisi/bigip/vs/*/*/clientside_max_conns           | conn
/jtlisi/bigip/vs/*/*/clientside_pkts_in             | pckt
/jtlisi/bigip/vs/*/*/clientside_pkts_out            | pckt
/jtlisi/bigip/vs/*/*/clientside_slow_killed         | conn
/jtlisi/bigip/vs/*/*/clientside_tot_conns           | conn
/jtlisi/bigip/vs/*/*/cs_max_conn_dur                | s
/jtlisi/bigip/vs/*/*/cs_mean_conn_dur               | s
/jtlisi/bigip/vs/*/*/cs_min_conn_dur                | s
/jtlisi/bigip/vs/*/*/ephemeral_bytes_in             | B
/jtlisi/bigip/vs/*/*/ephemeral_bytes_out            | B
/jtlisi/bigip/vs/*/*/ephemeral_cur_conns            | B
/jtlisi/bigip/vs/*/*/ephemeral_evicted_conns        | conn
/jtlisi/bigip/vs/*/*/ephemeral_max_conns            | conn
/jtlisi/bigip/vs/*/*/ephemeral_pkts_in              | pckt
/jtlisi/bigip/vs/*/*/ephemeral_pkts_out             | pckt
/jtlisi/bigip/vs/*/*/ephemeral_slow_killed          | conn
/jtlisi/bigip/vs/*/*/ephemeral_tot_conns            | conn
/jtlisi/bigip/vs/*/*/five_min_avg_usage_ratio       | event
/jtlisi/bigip/vs/*/*/five_sec_avg_usage_ratio       | event
/jtlisi/bigip/vs/*/*/one_min_avg_usage_ratio        | event
/jtlisi/bigip/vs/*/*/status_availability_state      | availability
/jtlisi/bigip/vs/*/*/syncookie_accepts              | event
/jtlisi/bigip/vs/*/*/syncookie_hw_accepts           | event
/jtlisi/bigip/vs/*/*/syncookie_hw_syncookies        | event
/jtlisi/bigip/vs/*/*/syncookie_hwsyncookie_instance | event
/jtlisi/bigip/vs/*/*/syncookie_rejects              | event
/jtlisi/bigip/vs/*/*/syncookie_swsyncookie_instance | event
/jtlisi/bigip/vs/*/*/syncookie_syncache_curr        | event
/jtlisi/bigip/vs/*/*/syncookie_syncache_over        | event
/jtlisi/bigip/vs/*/*/syncookie_syncookies           | event
/jtlisi/bigip/vs/*/*/tot_requests                   | req
