---
title: 'CB_CONNECTION_INFO 結構 (Cbclient .h) '
description: 包含連入連線要求的相關資訊。
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO 結構遠端桌面服務
- PCB_CONNECTION_INFO 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384213"
---
# <a name="cb_connection_info-structure"></a>CB \_ 連接 \_ 資訊結構

包含連入連線要求的相關資訊。 此結構會搭配 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法使用。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**使用者名稱**
</dt> <dd>

要求會話之使用者的名稱。

</dd> <dt>

**網域**
</dt> <dd>

使用者 **名稱為其** 成員之網域的名稱。

</dd> <dt>

**InitialProgram**
</dt> <dd>

啟動會話時啟動之初始程式的完整路徑和檔案名。 如果不應該啟動任何初始程式，請將這個成員設定為空字串。

</dd> <dt>

**Resource**
</dt> <dd>

[**CB \_ 資源 \_ 類型**](cb-resource-type.md)列舉值，指定連入連接所連接的資源類型。 如果 **PluginName** 成員為 **Null**，遠端桌面連線代理人會使用這個成員來判斷要叫用哪個外掛程式來判斷目的電腦。

</dd> <dt>

**PluginName**
</dt> <dd>

要叫用來判斷目的電腦之外掛程式的名稱。 如果此參數為 **Null**，則會使用 **資源** 成員來決定要叫用的外掛程式。

</dd> <dt>

**FarmName**
</dt> <dd>

包含電腦的伺服器陣列名稱稱，其中一個是將會重新導向連接的目的電腦。

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

這個成員保留供未來使用。

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

這個成員保留供未來使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





