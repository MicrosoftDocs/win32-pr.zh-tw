---
description: GetClassWindowStyles 方法會抓取視窗的類別樣式和視窗樣式。
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: 'CBaseWindow. GetClassWindowStyles 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074625"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>CBaseWindow. GetClassWindowStyles 方法

方法會抓取 `GetClassWindowStyles` 視窗的類別樣式和視窗樣式。

## <a name="syntax"></a>語法


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClassStyles* 
</dt> <dd>

接收類別樣式之變數的指標。

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

接收視窗樣式之變數的指標。

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

接收延伸視窗樣式之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含類別名稱的靜態文字字串。

## <a name="remarks"></a>備註

[**CBaseWindow：:P reparewindow**](cbasewindow-preparewindow.md)方法會呼叫這個方法，以取得視窗的類別樣式和視窗樣式。

這個方法是純虛擬的;衍生的類別必須加以執行。 下列範例顯示可能的實作為：


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



物件會針對 WNDCLASS 結構的 **lpszClassName** 成員（其會傳遞至 **RegisterClass** 函數）使用類別樣式。 物件使用 **CreateWindowEx** 函式的 *dwExStyle* 和 *dwStyle* 參數的視窗樣式。 如需詳細資訊，請參閱 Platform SDK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




