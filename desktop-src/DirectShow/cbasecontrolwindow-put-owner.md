---
description: Put \_ Owner 方法會設定影片視窗的父視窗; 父視窗接著會將某些訊息轉送至影片視窗。
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: 'CBaseControlWindow.put_Owner 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995452"
---
# <a name="cbasecontrolwindowput_owner-method"></a>CBaseControlWindow put \_ Owner 方法

`put_Owner`方法會設定影片視窗的父視窗; 父視窗接著會將某些訊息轉送至影片視窗。

## <a name="syntax"></a>語法


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*擁有者* 
</dt> <dd>

父視窗的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。

## <a name="remarks"></a>備註

就內部而言，這個方法會呼叫 Microsoft Win32 **SetParent** 函式來設定新的擁有者，並將父視窗的樣式設定為 WS \_ 子系。 父視窗接著會將特定的一組訊息轉寄 (特別是滑鼠和鍵盤訊息) 至影片視窗。

設定影片視窗的擁有者之後，您必須先將擁有者設為 **Null** ，並將擁有者的視窗樣式設定為 ws 重迭 \_ 和 ws CLIPCHILDREN，然後 \_ 再釋放篩選圖形。 當您將擁有者設為 **Null** 時，這個方法會關閉父視窗的 WS \_ 子位。 如果您未將擁有者設為 **Null**，父視窗會繼續將訊息傳遞至影片視窗，而且在應用程式關閉時可能會發生錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




