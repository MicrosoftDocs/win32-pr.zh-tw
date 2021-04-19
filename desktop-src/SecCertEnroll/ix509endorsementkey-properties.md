---
description: IX509EndorsementKey 介面會公開下列屬性。
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: IX509EndorsementKey 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989960"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="b9646-103">IX509EndorsementKey 屬性</span><span class="sxs-lookup"><span data-stu-id="b9646-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="b9646-104">[**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b9646-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b9646-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="b9646-105">In this section</span></span>



| <span data-ttu-id="b9646-106">主題</span><span class="sxs-lookup"><span data-stu-id="b9646-106">Topic</span></span>                                                                        | <span data-ttu-id="b9646-107">描述</span><span class="sxs-lookup"><span data-stu-id="b9646-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9646-108">**Length 屬性**</span><span class="sxs-lookup"><span data-stu-id="b9646-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="b9646-109">簽署金鑰的位長度。</span><span class="sxs-lookup"><span data-stu-id="b9646-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="b9646-110">您只能在呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法之後存取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b9646-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="b9646-111">**開啟的屬性**</span><span class="sxs-lookup"><span data-stu-id="b9646-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="b9646-112">指出是否已成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法。</span><span class="sxs-lookup"><span data-stu-id="b9646-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="b9646-113">**ProviderName 屬性**</span><span class="sxs-lookup"><span data-stu-id="b9646-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="b9646-114">加密提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9646-114">The name of the encryption provider.</span></span> <span data-ttu-id="b9646-115">預設值為 Microsoft 平臺密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="b9646-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="b9646-116">您必須先設定 [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) 屬性，然後再呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) 方法。</span><span class="sxs-lookup"><span data-stu-id="b9646-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="b9646-117">當您呼叫 **Open** 方法之後，就無法變更 **ProviderName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b9646-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




