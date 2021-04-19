---
title: IMsTscSecuredSettings StartProgram 屬性
description: 指定連接時要在遠端伺服器上啟動的程式。
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- StartProgram 屬性遠端桌面服務
- StartProgram 屬性遠端桌面服務，IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務，StartProgram 屬性
- StartProgram 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，StartProgram 屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966352"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a>IMsTscSecuredSettings：： StartProgram 屬性

指定連接時要在遠端伺服器上啟動的程式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a>屬性值

新啟動程式的名稱。 這個字串的最大長度為 **最大 \_ 路徑**-1 個字元。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如果未設定這個屬性的值，則會執行會話使用者的 shell 命令。 系統會從伺服器上的下列登錄值讀取 shell 命令：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **Shell**

如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings 定義為 c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





