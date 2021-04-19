---
description: MTP 擴充事件
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: MTP 擴充事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981686"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="e7564-103">MTP 擴充事件</span><span class="sxs-lookup"><span data-stu-id="e7564-103">MTP Extension Events</span></span>

<span data-ttu-id="e7564-104">事件會通知應用程式變更已發生在裝置上。</span><span class="sxs-lookup"><span data-stu-id="e7564-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="e7564-105">例如，應用程式可以註冊，以接收已移除裝置的通知。</span><span class="sxs-lookup"><span data-stu-id="e7564-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="e7564-106">廠商-擴充的事件代碼</span><span class="sxs-lookup"><span data-stu-id="e7564-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="e7564-107">當裝置製造商支援廠商擴充的事件時，其驅動程式會將廠商的事件程式碼 (UINT16) 與 **WPD \_ 事件 \_ MTP \_ 廠商 \_ 擴充 \_ 事件** GUID 的最高16位結合。</span><span class="sxs-lookup"><span data-stu-id="e7564-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="e7564-108">例如，如果廠商擴充的程式碼是0xC001，則產生的 GUID 會如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="e7564-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="e7564-109">廠商擴充的事件參數</span><span class="sxs-lookup"><span data-stu-id="e7564-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="e7564-110">廠商擴充事件的參數是由 **WPD \_ 事件 \_ 參數 \_ 事件 \_ 識別碼** GUID 和 **WPD \_ 屬性 \_ MTP \_ EXT \_ 事件 \_** 參數（ **PROPVARIANTS** 的集合）所報告。</span><span class="sxs-lookup"><span data-stu-id="e7564-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="e7564-111">這些 **PROPVARIANTS** 會對應到事件參數。</span><span class="sxs-lookup"><span data-stu-id="e7564-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="e7564-112">如果沒有參數，此集合會是空的。</span><span class="sxs-lookup"><span data-stu-id="e7564-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="e7564-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7564-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7564-114">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="e7564-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



