---
title: ITfCoNtextRenderingMarkup 介面
description: ITfCoNtextRenderingMarkup 介面是由 TSF 管理員所執行，並由應用程式使用。 您可以使用 ITfCoNtext 物件的 IQueryInterface 來抓取這個介面。 這個介面可協助應用程式列舉呈現資訊。
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfCoNtextRenderingMarkup 介面文字服務架構
- ITfCoNtextRenderingMarkup 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842467"
---
# <a name="itfcontextrenderingmarkup-interface"></a>ITfCoNtextRenderingMarkup 介面

**ITfCoNtextRenderingMarkup** 介面是由 TSF 管理員所執行，並由應用程式使用。 您可以使用 [ITfCoNtext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) 物件的 IQueryInterface 來抓取這個介面。 這個介面可協助應用程式列舉呈現資訊。



| ITfCoNtextRenderingMarkup 方法                                                | Description                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | 抓取指定範圍之轉譯標記的列舉值。 |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | 此函數並未實作。 它一律會傳回 E \_ >notimpl。       |



 

## <a name="members"></a>成員

**ITfCoNtextRenderingMarkup** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="remarks"></a>備註

> [!Note]  
> 這個介面目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

 