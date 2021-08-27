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
ms.openlocfilehash: d7ce04e38b41fce462973606f40f0099f010e6f4ab785900039e6771b0a9aaf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124848"
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

 

