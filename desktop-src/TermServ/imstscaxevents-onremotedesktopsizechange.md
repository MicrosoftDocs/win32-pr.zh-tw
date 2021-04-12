---
title: IMsTscAxEvents OnRemoteDesktopSizeChange 方法
description: 呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- OnRemoteDesktopSizeChange 方法遠端桌面服務
- OnRemoteDesktopSizeChange 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteDesktopSizeChange 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508759"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>IMsTscAxEvents：： OnRemoteDesktopSizeChange 方法

呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。

## <a name="syntax"></a>語法


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* \[在\]
</dt> <dd>

已調整大小之遠端桌面的寬度（以圖元為單位）。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

已調整大小之遠端桌面的高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此事件可讓容器判斷它是否必須自行調整大小以回應用戶端控制作業，這可能會導致更大的可見桌面大小。 請注意，此控制項將會自動調整新會話大小的捲軸。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





