---
title: IRemoteDesktopClientTouchPointer Enabled 屬性
description: RDP 應用程式容器用戶端控制項上是否啟用觸控指標功能。
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Enabled 屬性遠端桌面服務
- Enabled 屬性遠端桌面服務，IRemoteDesktopClientTouchPointer 介面
- IRemoteDesktopClientTouchPointer 介面遠端桌面服務，Enabled 屬性
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969793"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>IRemoteDesktopClientTouchPointer：： Enabled 屬性

RDP 應用程式容器用戶端控制項上是否啟用觸控指標功能。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>屬性值

如果已啟用觸控指標功能，則 **為 true** ;否則 **為 false**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                      |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ IRemoteDesktopClientTouchPointer 定義為260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

