---
description: 比較兩個數值資料類型實例或物件的兩個實例，以支援 < 的多載，並傳回兩個實例中較小的一個。 引數的資料類型和傳回值相同。
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: 'XMMin template (DirectXMath) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499853"
---
# <a name="xmmin-template"></a>XMMin 範本

比較兩個數值資料類型實例或物件的兩個實例，以支援 < 的多載，並傳回兩個實例中較小的一個。 引數的資料類型和傳回值相同。

## <a name="syntax"></a>語法

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="a"></span><span id="A"></span>*的*
</dt> <dd>

\[在中 \] ，指定兩個物件的第一個。

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[在中 \] ，指定兩個物件的其中兩個。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回兩個輸入物件中較小的一個。

## <a name="remarks"></a>備註

`XMMin` 是範本，而且在範本具現化時，會指定 T 類型。

> [!Note]  
> `XMMin`範本是 DirectXMath 的新功能，不適用於 XNAMath 2.x。 `XMMin` 可在 XNAMath 2.x 中以宏的形式提供。

 

> [!Note]  
> 在理想情況下，請使用 std：： min 而不是 `XMMin` 。 若要避免與 std：： min 的 Windows 標頭髮生衝突，您必須 \# 先定義 NOMINMAX，然後再包含 Windows 標頭。

 

**命名空間**：使用 DirectX

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 支援 Win32 傳統型應用程式、Windows 儲存應用程式，以及 Windows Phone 8 個應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DirectXMath。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectXMath 程式庫範本函數](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




