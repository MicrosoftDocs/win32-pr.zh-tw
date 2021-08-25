---
description: 包含用來取得用於連接服務之端點的方法。
ms.assetid: 4380776A-3B89-444B-B1E9-DCF640D0AEB4
title: IUpdateEndpointProvider 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider
api_type:
- COM
ms.openlocfilehash: 2242e30ccd64c0252d5a1ea97eedd865f9e80bee2c58f749ca6d2eabd64c6167
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896838"
---
# <a name="iupdateendpointprovider-interface"></a>IUpdateEndpointProvider 介面

包含用來取得用於連接服務之端點的方法。 此介面會在撰寫端點提供者時執行。

## <a name="members"></a>成員

**IUpdateEndpointProvider** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IUpdateEndpointProvider** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUpdateEndpointProvider** 介面具有這些方法。



| 方法                                                                       | 描述                                                           |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) | 要求用來連接到服務的端點。<br/> |



 

## <a name="remarks"></a>備註

WUA 會呼叫 [**GetServiceEndpoint**](iupdateendpointauthprovider-getserviceendpoint.md) 方法來啟動協調進程。 進行呼叫時，WUA 會傳入已註冊的權杖類型，而此介面的執行會傳回它慣用使用的權杖類型。

 

 
