---
title: ITfCoNtextRenderingMarkup GetRenderingMarkup 方法
description: ITfCoNtextRenderingMarkup GetRenderingMarkup 方法會抓取指定範圍之轉譯標記的列舉值。
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- GetRenderingMarkup 方法文字服務架構
- GetRenderingMarkup 方法文字服務架構，ITfCoNtextRenderingMarkup 介面
- ITfCoNtextRenderingMarkup 介面文字服務架構，GetRenderingMarkup 方法
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682671"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a>ITfCoNtextRenderingMarkup：： GetRenderingMarkup 方法

**ITfCoNtextRenderingMarkup：： GetRenderingMarkup** 方法會抓取指定範圍之轉譯標記的列舉值。

## <a name="syntax"></a>語法


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ec* \[在\]
</dt> <dd>

\[\]以唯讀的編輯 cookie 來存取內容。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

\[in\]



| 值                                                                                                                                                                                         | 意義                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <dt>**TF \_ GRM \_ INCLUDE \_ 屬性**</dt> </dl> | 如果這個位為1，則列舉值將包含 GUID 屬性屬性（ \_ \_ property）。<br/> |



 

</dd> <dt>

*pRangeCover* \[在\]
</dt> <dd>

\[在指向 \] 範圍之 [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) 介面的指標中，以列舉呈現標記。

</dd> <dt>

*ppEnum* \[擴展\]
</dt> <dd>

\[取出 \] 指標以取得 [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                | 描述                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法成功。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個方法目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

