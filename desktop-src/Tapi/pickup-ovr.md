---
description: 取貨作業可讓應用程式回答在另一個位址發出警示的會話。 應用程式會識別取貨的目標，並傳回所挑選通話的會話識別碼。
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: 皮卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694199"
---
# <a name="pickup"></a>皮卡

取貨作業可讓應用程式回答在另一個位址發出警示的會話。 應用程式會識別取貨的目標，並傳回所挑選通話的會話識別碼。

有幾種方式可以識別取貨要求的目標。 首先，應用程式可以指定警示合作物件的位址。 其次，如果未指定位址，而且參數允許，則應用程式可以在其收取群組中挑選任何警示會話。 第三，如果指定了群組識別碼，某些參數允許在不同的取貨群組中收取會話警示。

某些重要的電話系統支援 *透過保留* 功能，在橋接專屬通話外觀上進行轉移。 在此配置中，特定的電話會在撥打電話時獨佔呼叫，但是當通話處於待命狀態時，任何有該行外觀的電話都可以收取通話。

**TAPI 2.x：** 應用程式可以使用具有 **Null** 目標位址的收取作業來達到此目的，類似于如何使用函式來挑選類比線路上的呼叫等候呼叫。 LINEADDRFEATURE \_ PICKUPHELD 指出功能是否存在。

如果 LINEADDRCAPFLAGS \_ PICKUPCALLWAIT 為 **TRUE**，則可挑選使用者已語音偵測到呼叫等候信號的會話，但服務提供者無法執行偵測。 這樣一來，即使服務提供者無法偵測來電等候信號，使用者也可以使用「回答」等待來電的機制。 目的地位址和群組識別碼都必須是 **Null** ，才能收取通話等候的呼叫。

成功挑選會話之後，應用程式會收到狀態變更通知， [原因](reason-ovr.md) 是設定為 LINECALLREASON \_ 取貨。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup)。

 

 
