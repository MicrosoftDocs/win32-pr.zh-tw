---
title: 網路管理功能
description: 網路管理功能可以依下列方式分組。
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "106966897"
---
# <a name="network-management-functions"></a>網路管理功能

網路管理功能可以依下列方式分組。

## <a name="alert-functions"></a>警示功能



| 函式                                   | 描述                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | 通知所有已註冊的用戶端發生特定事件。                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | 簡化通知已註冊的用戶端發生特定事件，因為不同于 **NetAlertRaise**， **NetAlertRaiseEx** 不需要 [**STD \_ 警示**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) 結構。 |



 

## <a name="api-buffer-functions"></a>API 緩衝區函式



| 函式                                                 | 描述                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | 從堆積配置記憶體。 當您需要與 **NetApiBufferFree** 函數相容時，請呼叫此函數。 |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | 釋放 **NetApiBufferAllocate** 函式所配置的記憶體和其他網路管理功能。                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | 變更 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小。                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | 傳回對 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小（以位元組為單位）。                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory 聯結資訊函數



| 函式                                                       | 描述                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | 釋出針對指定的 [**DSREG \_ 聯結 \_ 資訊**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) 結構所配置的記憶體，其中包含租使用者的聯結資訊，以及藉由呼叫 [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) 函式而取出的資訊。 |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | 抓取指定租使用者的聯結資訊。 此函數會檢查 Microsoft Azure Active Directory 的聯結資訊，以及目前使用者加入的工作帳戶。                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>目錄服務和網域加入功能



| 函式                                                                             | 描述                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | 為指定的電腦新增替代名稱。                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | 布建電腦帳戶以供稍後用於離線網域加入作業。                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | 列舉指定電腦的名稱。                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | 抓取組織單位清單， (Ou) 可在其中建立電腦帳戶。                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | 抓取指定電腦的聯結狀態資訊。                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | 將電腦加入工作組或網域。                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | 布建電腦帳戶，以供稍後用於離線網域加入作業。                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | 移除指定電腦的替代名稱。                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | 變更網域中的電腦名稱稱。                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | 在本機電腦上執行，以修改磁片區上所裝載的 Windows 作業系統映射。 系統會載入映射的登錄，並寫入布建 blob 資料，以便在離線網域加入作業的完成階段進行取出。     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | 在本機電腦上執行，以修改磁片區上所裝載的 Windows 作業系統映射。 系統會從映射載入登錄，並寫入布建套件資料，以便在離線網域加入作業的完成階段進行取出。 |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | 設定指定電腦的主要電腦名稱稱。                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Unjoins 工作組或網域中的電腦。                                                                                                                                                                                                                        |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | 確認電腦名稱稱、工作組名稱或功能變數名稱的有效性。                                                                                                                                                                                               |



 

## <a name="get-functions"></a>取得函式



| 函式                                                               | 描述                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | 傳回指定伺服器直接信任之網域的任何網域控制站的名稱。                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | 針對指定的網域，傳回網域主控站 (PDC) 的名稱。                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | 傳回第一個顯示資訊專案的索引，其名稱開頭為指定的字串或依字母順序排列在字串後面。 |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | 傳回使用者、電腦或通用群組帳戶資訊。                                                                             |



 

## <a name="group-functions"></a>群組函式



| 函式                                     | 描述                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | 建立全域群組。                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | 將一位使用者新增至現有的全域群組。                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | 移除群組是否有任何成員的全域群組。                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | 從全域群組移除一個使用者名稱。                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | 列出伺服器上的所有全域群組。                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | 傳回特定全域群組的相關資訊。                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | 列出特定全域群組的所有成員。                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | 設定全域群組的一般資訊。                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | 指派成員給新的全域群組;取代現有群組的成員。 |



 

## <a name="local-group-functions"></a>本機群組函數



| 函式                                                   | 描述                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | 建立本機群組。                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | 將一或多個使用者或全域群組新增至現有的本機群組。     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | 刪除本機群組，從群組中移除所有現有的成員。    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | 從現有的本機群組移除一或多個成員。               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | 傳回伺服器上每個本機群組帳戶的相關資訊。         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | 傳回伺服器上特定本機群組帳戶的相關資訊。 |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | 列出指定之本機群組的所有成員。                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | 設定有關本機群組的一般資訊。                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | 指派成員到本機群組。                                       |



 

## <a name="message-functions"></a>訊息函數



| 函式                                               | 描述                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | 將訊息傳送至已註冊的訊息別名。                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | 在訊息名稱資料表中註冊訊息別名。                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | 從訊息名稱資料表刪除訊息別名。                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | 列出儲存在訊息名稱資料表中的所有訊息別名。                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | 傳回訊息名稱資料表中特定訊息別名的相關資訊。 |



 

## <a name="netfile-functions"></a>NetFile 函式



| 函式                                | 描述                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | 強制關閉資源。                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | 傳回伺服器上開啟之檔案的相關資訊。                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | 傳回伺服器資源特定開啟的相關資訊。 |



 

## <a name="remote-utility-functions"></a>遠端公用程式函式



| 函式                                                       | 描述                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | 查詢重新導向器，以取得遠端系統支援的選用功能。 |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | 可讓應用程式存取遠端伺服器上的當日時間資訊。          |



 

## <a name="schedule-functions"></a>排程函數



| 函式                                                                     | 描述                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | 提交工作，以在指定的未來日期和時間執行。        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | 取消佇列中要在電腦上執行的工作範圍。             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | 列出在指定電腦上佇列的作業。                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | 傳回在電腦上佇列的特定作業的相關資訊。 |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | 捕獲 AT 服務帳戶名稱。                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | 設定 AT 服務帳戶名稱和密碼。                   |



 

## <a name="server-functions"></a>伺服器函數



| 函式                                       | 描述                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | 傳回伺服器上的本機磁片磁碟機清單。                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | 列出特定類型的所有可見伺服器 (或指定網域中) 的類型。 |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | 傳回指定伺服器的設定資訊。                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | 設定伺服器的指令引數。                                        |



 

## <a name="server-and-workstation-transport-functions"></a>伺服器和工作站傳輸功能



| 函式                                                     | 描述                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | 將模擬的伺服器名稱系結至伺服器使用中的每個傳輸通訊協定。  (結合 [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) 函式和 [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) 函數的功能。 )                                             |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | 將每個網路傳輸通訊協定與先前呼叫 **NetServerComputerNameAdd** 函式所設定的模擬伺服器名稱中斷連線。                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | 將指定的伺服器系結至傳輸通訊協定。  (此函式只支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) 資訊層級。 )                                                                                                                                                 |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | 將指定的伺服器系結至傳輸通訊協定。  (此擴充功能可支援 [**伺服器 \_ 傳輸 \_ 資訊 \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)、 [**伺服器 \_ 傳輸 \_ 資訊 \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)和 [**伺服器 \_ 傳輸資訊 \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) 資訊層級。 )  |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | 中斷傳輸通訊協定與伺服器的連線。                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | 列舉伺服器所管理的傳輸通訊協定。                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | 列出由重新導向程式管理的傳輸通訊協定。                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>使用函式



| 函式                               | 描述                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | 在本機電腦與伺服器之間建立連線。                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | 結束共用資源的連接。                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | 列出本機電腦與遠端伺服器上的資源之間的所有目前連接。 |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | 傳回共用資源連接的相關資訊。                              |



 

## <a name="user-functions"></a>使用者函式



| 函式                                               | 描述                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | 新增使用者帳戶，並指派密碼和許可權層級。     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | 變更指定網路伺服器或網域的使用者密碼。 |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | 從伺服器刪除使用者帳戶。                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | 列出伺服器上的所有使用者帳戶。                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | 傳回使用者所屬通用群組名的清單。       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | 傳回伺服器上特定使用者帳戶的相關資訊。    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | 傳回使用者所屬的本機群組名稱清單。        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | 設定指定之使用者帳戶的全域群組成員資格。         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | 設定使用者帳戶的密碼和其他元素。             |



 

## <a name="user-modals-functions"></a>使用者 Modals 函式



| 函式                                     | 描述                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | 傳回安全性資料庫中所有使用者和全域群組的全域資訊，也就是安全性帳戶管理員 (SAM) 資料庫，或在網域控制站的情況下 Active Directory。 |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | 針對安全性資料庫中的所有使用者和全域群組設定全域資訊。                                                                                                                       |



 

## <a name="validation-functions"></a>驗證函式



| 函式                                                               | 描述                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | 釋出 [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) 函式為 *OutputArg* 參數配置的記憶體，                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | 讓應用程式能夠根據應用程式提供的帳戶資料庫檢查密碼合規性，並確認密碼符合密碼原則的複雜度、過時、最小長度和歷程記錄重複使用需求。 |



 

## <a name="workstation-and-workstation-user-functions"></a>工作站和工作站使用者功能



| 函式                                           | 描述                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | 傳回工作站設定元素的相關資訊。             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | 設定工作站。                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | 列出所有目前登入工作站的使用者的相關資訊。           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | 傳回一個目前登入使用者的相關資訊。                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | 設定工作站設定元素的使用者特定資訊。 |



 

## <a name="obsolete-functions"></a>過時的函式

-   [**NetAccessAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**NetConfigSet**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 網路功能](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 