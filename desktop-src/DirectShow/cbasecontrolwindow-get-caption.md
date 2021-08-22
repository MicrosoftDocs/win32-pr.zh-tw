---
description: 取得 \_ 標題方法會抓取目前的視窗標題。
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: 'CBaseControlWindow.get_Caption 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640887"
---
# <a name="cbasecontrolwindowget_caption-method"></a>CBaseControlWindow. 取得 \_ Caption 方法

方法會抓取 `get_Caption` 目前的視窗標題。

## <a name="syntax"></a>語法


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrCaption* 
</dt> <dd>

目前視窗標題的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

以 Windows 為基礎的桌面最上層視窗會有相關聯的標題 (標題) 。 您可以透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面來查詢和設定這個屬性。 只有在視窗已套用 WS 標題樣式時，才會顯示任何標題集 \_ 。 如果沒有，標題仍可 (設定，並) 抓取，但使用者看不到它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




