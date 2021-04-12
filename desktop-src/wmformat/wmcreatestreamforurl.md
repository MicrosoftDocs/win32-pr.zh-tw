---
title: WMCreateStreamForURL 函式
description: WMCreateStreamForURL 函式是由應用程式所執行，以建立指定 URL 的 COM IStream 物件。
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- WMCreateStreamForURL 函式 windows Media 格式
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373137"
---
# <a name="wmcreatestreamforurl-function"></a>WMCreateStreamForURL 函式

**WMCreateStreamForURL** 函式是由應用程式所執行，以建立指定 URL 的 COM **IStream** 物件。

## <a name="syntax"></a>語法


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszURL* \[在\]
</dt> <dd>

包含 URL 的寬字元字串的指標。

</dd> <dt>

*pfCorrectSource* \[擴展\]
</dt> <dd>

旗標的指標，true 將會防止 SDK 嘗試此 URL 的其他來源外掛程式。

</dd> <dt>

*ppStream* \[擴展\]
</dt> <dd>

方法所建立之 **IStream** 物件指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它必須傳回 S \_ OK。 如果失敗，則必須傳回適當的 **HRESULT** 錯誤碼，而且 \* *PpStream* 應該設為 **Null**。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**來源外掛程式**](source-plug-ins.md)
</dt> </dl>

 

 




