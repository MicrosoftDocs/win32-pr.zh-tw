---
title: TF_RENDERINGMARKUP 結構
description: TF \_ RENDERINGMARKUP 結構結構包含範圍和顯示內容資訊。
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP 結構文字服務架構
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968262"
---
# <a name="tf_renderingmarkup-structure"></a>TF \_ RENDERINGMARKUP 結構

[**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color)結構結構包含範圍和顯示內容資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>成員

<dl> <dt>

**pRange**
</dt> <dd>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)介面的指標。

</dd> <dt>

**tfDisplayAttr**
</dt> <dd>

顯示內容資訊。

</dd> </dl>

## <a name="remarks"></a>備註

此結構目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 




