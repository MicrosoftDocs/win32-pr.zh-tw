---
title: 取得連結識別碼
description: 從 Windows Server 2003 開始，不再需要向 Microsoft 要求 linkID;自動產生 linkID 的流程。
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- 取得連結識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092631"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="9bf34-104">取得連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9bf34-104">Obtaining a Link ID</span></span>

<span data-ttu-id="9bf34-105">從 Windows Server 2003 開始，不再需要向 Microsoft 要求 [**linkID**](/windows/desktop/ADSchema/a-linkid) ;自動產生 **linkID** 的流程。</span><span class="sxs-lookup"><span data-stu-id="9bf34-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="9bf34-106">當屬性的 **linkID** 屬性設定為1.2.840.113556.1.2.50 時，系統會自動為新的連結屬性產生連結識別碼。</span><span class="sxs-lookup"><span data-stu-id="9bf34-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="9bf34-107">將 **linkID** 設定為轉寄連結的 [**attributeID**](/windows/desktop/ADSchema/a-attributeid) 或 [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) ，即可建立此轉寄連結的上一頁連結。</span><span class="sxs-lookup"><span data-stu-id="9bf34-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="9bf34-108">在建立轉寄連結之後，以及建立後置連結之前，必須重載架構快取。</span><span class="sxs-lookup"><span data-stu-id="9bf34-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="9bf34-109">否則，就不會在建立後置連結時找到轉寄連結的 **attributeId** 或 **ldapDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="9bf34-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="9bf34-110">架構快取是在進行架構變更後的幾分鐘內，或是在重新開機 DC 時，視需要重載。</span><span class="sxs-lookup"><span data-stu-id="9bf34-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="9bf34-111">建立所有轉寄連結、重載架構快取，然後建立所有的上一頁連結。</span><span class="sxs-lookup"><span data-stu-id="9bf34-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="9bf34-112">例如，當您建立新的屬性 **myForwardLinkAttr** 和 **myBackLinkAttr**，並想要將它們連結：</span><span class="sxs-lookup"><span data-stu-id="9bf34-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="9bf34-113">此範例中的 Oid 是假設。</span><span class="sxs-lookup"><span data-stu-id="9bf34-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="9bf34-114">如需取得新屬性之 Oid 的指示，請參閱 [從 Microsoft 取得物件識別碼](obtaining-an-object-identifier-from-microsoft.md) 。</span><span class="sxs-lookup"><span data-stu-id="9bf34-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="9bf34-115">在要作為轉寄連結的屬性上，設定這些屬性：</span><span class="sxs-lookup"><span data-stu-id="9bf34-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="9bf34-116">重載架構。</span><span class="sxs-lookup"><span data-stu-id="9bf34-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="9bf34-117">在要做為後置連結的屬性上，設定這些屬性：</span><span class="sxs-lookup"><span data-stu-id="9bf34-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9bf34-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="9bf34-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf34-119">連結屬性</span><span class="sxs-lookup"><span data-stu-id="9bf34-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="9bf34-120">如何延伸架構</span><span class="sxs-lookup"><span data-stu-id="9bf34-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 