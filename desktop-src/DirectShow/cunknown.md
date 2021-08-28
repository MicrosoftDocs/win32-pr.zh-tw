---
description: CUnknown 類別會實作為 IUnknown 介面。 大部分的元件物件模型 (DirectShow 衍生自 CUnknown 的 COM) 物件。
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: 'CUnknown 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075991"
---
# <a name="cunknown-class"></a>CUnknown 類別

![cunknown 類別階層](images/cbase01.png)

**CUnknown** 類別會實作為 **IUnknown** 介面。 大部分的元件物件模型 (DirectShow 衍生自 **CUnknown** 的 COM) 物件。

如果您執行的是 COM 物件，您可能會想要從 **CUnknown** 衍生。 衍生自 **CUnknown** 可提供安全線程的執行，並可讓您省下執行 **IUnknown** 的麻煩。

如需如何使用此基類的詳細討論，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。 以下是簡短摘要：

-   在您類別定義的公用區段中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏。 此宏會宣告 **IUnknown** 介面的三種方法。
-   覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法以支援 **IUnknown** 以外的介面。 在這個方法中，呼叫 [**GetInterface**](getinterface.md) 函式來取出介面指標。
-   在類別的函式中，叫用 **CUnknown** 的方法。



| 受保護的成員變數                                                  | 描述                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cRef**](cunknown-m-cref.md)                                          | 參考計數。                                                   |
| 公用方法                                                              | 描述                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | 函式方法。                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | 函式方法。 虛擬。                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | 取得控制 **IUnknown** 的指標。                    |
| INonDelegatingUnknown 方法                                               | 描述                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | 遞增參考計數。                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | 捕獲介面指標並遞增參考計數。 |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | 遞減參考計數。                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> </dl>

 

 




