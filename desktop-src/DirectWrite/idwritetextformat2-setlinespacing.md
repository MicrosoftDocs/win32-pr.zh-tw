---
title: IDWriteTextFormat2 SetLineSpacing 方法
description: 設定行間距。 |IDWriteTextFormat2 SetLineSpacing 方法
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- SetLineSpacing 方法直接寫入
- SetLineSpacing 方法 Direct Write，IDWriteTextFormat2 介面
- IDWriteTextFormat2 介面 Direct Write，SetLineSpacing 方法
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196110"
---
# <a name="idwritetextformat2setlinespacing-method"></a>IDWriteTextFormat2：： SetLineSpacing 方法

設定行間距。

## <a name="syntax"></a>語法


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lineSpacingOptions* \[在\]
</dt> <dd>

Type： **Const [**DWRITE \_ \_**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \*** 行距

如何管理各行之間的空間。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                 |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextFormat2**](idwritetextformat2.md)
</dt> </dl>

 

 





