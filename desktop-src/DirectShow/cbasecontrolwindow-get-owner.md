---
description: 取得擁有者方法會抓取 \_ 目前的視窗擁有者。
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: 'CBaseControlWindow.get_Owner 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660511"
---
# <a name="cbasecontrolwindowget_owner-method"></a>CBaseControlWindow 取得 \_ Owner 方法

方法會抓取 `get_Owner` 目前的視窗擁有者。

## <a name="syntax"></a>語法


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*擁有者* 
</dt> <dd>

視窗擁有者的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

影片視窗可以在檔環境內播放。 若要這樣做，必須將視窗設為另一個視窗 (的子系，以便將其裁剪並適當地移) 。 這個屬性可讓您設定和取出視窗的擁有者。 當視窗由另一個視窗所擁有時，它只會呼叫 Microsoft Win32 **SetParent** 函式。 呼叫此函式的應用程式將會變更視窗樣式，以 \_ 在上設定 WS 子位。

當視窗由另一個視窗所擁有時，會自動將特定的訊息集轉寄 (特別是) 的滑鼠和鍵盤訊息。 這可讓應用程式進行簡單的熱點編輯和其他互動。

此成員函式的目的是要透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面呼叫外部物件，因此會鎖定重要區段以與相關聯的篩選進行同步處理。 呼叫 [**CBaseControlWindow：： GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) 成員函式，以取得此屬性（如果不是從外部物件呼叫）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




