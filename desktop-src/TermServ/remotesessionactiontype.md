---
title: RemoteSessionActionType 列舉
description: 用來指定遠端動作的類型。
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- RemoteSessionActionType 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967324"
---
# <a name="remotesessionactiontype-enumeration"></a>RemoteSessionActionType 列舉

用來指定遠端動作的類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**
</dt> <dd>

顯示遠端會話中的常用鍵。

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**
</dt> <dd>

在遠端會話中顯示應用程式行。

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**
</dt> <dd>

將應用程式停駐在遠端會話中。 此選項已被取代，不應該使用。

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**
</dt> <dd>

使開始畫面顯示在遠端會話中。

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**
</dt> <dd>

使應用程式切換視窗顯示在遠端會話中。 這與按下 Alt + Tab 鍵的使用者相同。

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**
</dt> <dd>

使動作中心顯示在遠端會話中。 這與按下 Win + A 的使用者相同。

**Windows server 2012 R2、Windows 8.1、Windows server 2012 和 Windows 8：** 在 Windows Server 2016 和 Windows 10 之前，不支援這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient8::SendRemoteAction**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





