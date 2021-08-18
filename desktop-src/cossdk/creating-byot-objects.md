---
description: 建立 BYOT 物件
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: 建立 BYOT 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128761"
---
# <a name="creating-byot-objects"></a>建立 BYOT 物件

新的 BYOT 物件會建立具有手動交易的物件。 [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex)和 [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)這兩個介面具有單一方法 **CreateInstance**，分別採用 **ITransaction** 介面指標和提示 URL。 [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) 會將介面指標傳回至新建立的物件，該物件會在指定的交易中登記。

釋放具有手動交易的物件時，COM + 不會嘗試認可交易。 交易是由外部交易管理員明確控制，該管理員會將建立此物件的交易分配給該交易。

> [!Note]  
> 必須將 Byot. ByotServerEx 物件匯入至 COM + 應用程式。

 

 

 



