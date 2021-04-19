---
title: IMsTscSecuredSettings WorkDir 屬性
description: 指定啟動程式的工作目錄。
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- WorkDir 屬性遠端桌面服務
- WorkDir 屬性遠端桌面服務，IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務，WorkDir 屬性
- WorkDir 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，WorkDir 屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966351"
---
# <a name="imstscsecuredsettingsworkdir-property"></a>IMsTscSecuredSettings：： WorkDir 屬性

指定啟動程式的工作目錄。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a>屬性值

新的工作目錄。 這個字串的最大長度為 **最大 \_ 路徑**-1 個字元。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

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

 

 





