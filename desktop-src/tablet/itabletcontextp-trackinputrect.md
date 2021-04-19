---
description: 將 tablet 數位板更新為視窗位置對應座標。
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: ITabletCoNtextP：： TrackInputRect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985343"
---
# <a name="itabletcontextptrackinputrect-method"></a>ITabletCoNtextP：： TrackInputRect 方法

將 tablet 數位板更新為視窗位置對應座標。

## <a name="syntax"></a>語法


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prcInput* \[擴展\]
</dt> <dd>

在更新視窗和數位板座標之間的對應之後，新的輸入視窗矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

每當畫面上視窗的位置變更時，就呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCoNtextP 介面**](itabletcontextp.md)
</dt> </dl>

 

 




