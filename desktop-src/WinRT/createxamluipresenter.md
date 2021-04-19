---
description: 靜態 creator 函式，可在桌面應用程式中建立呈現介面的 XamlUIPresenter。
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995108"
---
# <a name="createxamluipresenter-function"></a>CreateXamlUIPresenter 函式

靜態 creator 函式，可在桌面應用程式中建立呈現介面的 [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) 。

## <a name="syntax"></a>語法


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPresentSite* \[在\]
</dt> <dd>

現有的裝載介面。 請參閱 Internet Explorer 檔中的 **IViewObjectPresentNotifySite** 。

</dd> <dt>

*ppPresenter* \[擴展\]
</dt> <dd>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)的 **\[ exclusiveto \]** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

標準 **HResult**， **S \_ 正常** ，表示成功。

## <a name="remarks"></a>備註

呼叫這個方法需要 Windows.UI.Xaml.dll 的 **DllImport** 。

您無法從 Windows Store 應用程式呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Xaml-coretypes .idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
