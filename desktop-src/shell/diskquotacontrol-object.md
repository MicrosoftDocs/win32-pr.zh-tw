---
description: 可讓系統管理員管理磁片區的磁片配額屬性。
title: DiskQuotaControl 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841549"
---
# <a name="diskquotacontrol-object"></a>DiskQuotaControl 物件

可讓系統管理員管理磁片區的磁片配額屬性。 NTFS 檔案系統可讓系統管理員藉由為每個使用者配置指定的磁碟空間數量或 *配額限制*，來管理共用磁片區上的磁片使用量。 您可以使用此物件來設定將自動指派給所有新使用者的預設配額限制。

## <a name="members"></a>成員

**DiskQuotaControl** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**DiskQuotaControl** 物件具有這些事件。



| 事件                                                           | 描述                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | 當已解析 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的名稱資訊時發生。<br/> |



 

### <a name="methods"></a>方法

**DiskQuotaControl** 物件有這些方法。



| 方法                                                                                    | 描述                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | 將非預設磁片配額指派給新的使用者。<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | 從磁片區刪除使用者。<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | 在磁片區的配額檔案中，依名稱尋找使用者的專案。<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | 將指定的使用者物件放在行中，以進行名稱解析。<br/>              |
| [**初始化**](diskquotacontrol-initialize.md)                                         | 開啟指定的磁片區，並初始化其配額控制物件。<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | 使安全性識別碼的使用者名稱快取失效。<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | 關閉使用者名稱解析執行緒。<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | 以字串格式將登入名稱轉譯為對應的使用者安全識別碼。<br/> |



 

### <a name="properties"></a>屬性

**DiskQuotaControl** 物件具有這些屬性。



| 屬性                                                                                   | 存取類型           | 描述                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | 讀取/寫入<br/> | 設定或取得預設配額限制。<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | 唯讀<br/>  | 取得做為文字字串的預設配額限制。<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | 讀取/寫入<br/> | 設定或取得預設配額閾值。<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | 唯讀<br/>  | 取得預設配額閾值做為文字字串。<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | 讀取/寫入<br/> | 設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | 讀取/寫入<br/> | 設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | 唯讀<br/>  | 取得布林值，這個值會指出磁片區的配額檔案是否已完成。<br/>                                                             |
| [**QuotaFileRebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | 唯讀<br/>  | 取得布林值，指出目前是否正在重建磁片區的配額檔案。<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | 讀取/寫入<br/> | 設定或取得磁片區磁片配額的狀態。<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | 讀取/寫入<br/> | 設定或取得值，這個值會控制如何將使用者 SID 解析為使用者名稱。<br/>                                                                        |



 

## <a name="remarks"></a>備註

系統管理員可以使用 **DiskQuotaControl** 物件來執行一些工作，包括下列各項：

-   啟用和停用磁片區的磁片配額系統。
-   取得磁片區上配額系統的狀態。
-   拒絕超過配額限制的使用者磁碟空間。
-   指定預設的警告臨界值，以及將指派給新使用者的配額限制值。
-   新增和移除使用者。

**DiskQuotaControl** 物件可讓您設定磁片區的全域預設值，例如配額限制。 不過，每個使用者都是由可用來指定個別配額設定的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件表示。

有幾種方式可以取得使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件：

-   具有磁片區配額之所有使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件會公開為集合，而且可以列舉。 如需有關如何列舉 **DIDiskQuotaUser** 物件的討論，請參閱 **DIDiskQuotaUser** 的「備註」一節中的「**列舉磁片配額使用者**」。
-   當您加入新的使用者時， [**AddUser**](diskquotacontrol-adduser.md) 方法會傳回使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。
-   如果您有使用者的名稱， [**FindUser**](diskquotacontrol-finduser.md) 方法會傳回使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。

這個物件讓 IDiskQuotaControl 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Shell 物件**](shell.md)
</dt> </dl>

 

 




