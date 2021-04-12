---
title: 字碼頁和 Unicode 字串
description: 執行 IPropertySetStorage 的另一個考慮是如何將 Unicode 屬性名稱儲存在屬性識別碼 0 (屬性名稱字典) ，而不會使用 Unicode 字串。
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- 字碼頁和 Unicode 字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300239"
---
# <a name="code-pages-and-unicode-strings"></a><span data-ttu-id="89c0b-104">字碼頁和 Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="89c0b-104">Code Pages and Unicode Strings</span></span>

<span data-ttu-id="89c0b-105">執行 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的另一個考慮是如何將 Unicode 屬性名稱儲存在屬性識別碼 0 (屬性名稱字典) ，而不會使用 unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="89c0b-105">Another consideration in implementing [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is how Unicode property names are stored in the property ID 0 (the property name dictionary), which does not use Unicode strings.</span></span>

<span data-ttu-id="89c0b-106">Unicode 正式具有字碼頁值1200。</span><span class="sxs-lookup"><span data-stu-id="89c0b-106">Unicode officially has a code page value of 1200.</span></span> <span data-ttu-id="89c0b-107">若要將 Unicode 值儲存在屬性名稱字典中，請針對屬性識別碼1中的整個屬性集 (使用1200的字碼頁值) ，並在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)中缺少 **PROPSETFLAG \_ ANSI** 旗標所指定。</span><span class="sxs-lookup"><span data-stu-id="89c0b-107">To store Unicode values in the property name dictionary, use a code page value of 1200 for the whole property set (in property ID 1), specified by the absence of the **PROPSETFLAG\_ANSI** flag in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span></span> <span data-ttu-id="89c0b-108">請注意，這會有將所有字串值以 Unicode 儲存在屬性集中的副作用。</span><span class="sxs-lookup"><span data-stu-id="89c0b-108">Be aware that this has the side effect of storing all string values in the property set in Unicode.</span></span> <span data-ttu-id="89c0b-109">在所有字碼頁中，在 **VT \_ LPSTR** 的開頭找到的計數是位元組計數，而非字元計數。</span><span class="sxs-lookup"><span data-stu-id="89c0b-109">In all code pages, the count found at the start of a **VT\_LPSTR** is a byte count, not a character count.</span></span> <span data-ttu-id="89c0b-110">為了提供與舊版用戶端的相容性，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="89c0b-110">This is necessary to provide for compatibility with earlier-version clients.</span></span>

<span data-ttu-id="89c0b-111">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的複合檔案執行會以 Unicode (字碼頁 1200) 或在目前的系統 ANSI 字碼頁中，完全建立所有新的屬性集。</span><span class="sxs-lookup"><span data-stu-id="89c0b-111">The compound file implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates all new property sets completely either in Unicode (code page 1200) or in the current system ANSI code page.</span></span> <span data-ttu-id="89c0b-112">這是由 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *grfFlags* 參數中的 **PROPSETFLAG \_ ANSI** 旗標缺少或存在所控制。</span><span class="sxs-lookup"><span data-stu-id="89c0b-112">This is controlled by the absence or presence of the **PROPSETFLAG\_ANSI** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span></span>

<span data-ttu-id="89c0b-113">建立並開啟屬性集作為 Unicode。</span><span class="sxs-lookup"><span data-stu-id="89c0b-113">Create and open property sets as Unicode.</span></span> <span data-ttu-id="89c0b-114">若要執行這項操作，請勿在 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的 *grfFlags* 參數中設定 **PROPSETFLAG \_ ANSI** 旗標。</span><span class="sxs-lookup"><span data-stu-id="89c0b-114">To implement this, do not set the **PROPSETFLAG\_ANSI** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span></span> <span data-ttu-id="89c0b-115">避免使用 **vt \_ LPSTR** 值，而改為使用 **vt \_ LPWSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="89c0b-115">Avoid using **VT\_LPSTR** values, and instead use **VT\_LPWSTR** values.</span></span> <span data-ttu-id="89c0b-116">當屬性設定的字碼頁是 Unicode 時， **VT \_ LPSTR** 字串值會在儲存時轉換成 unicode，並在抓取時轉換回多位元組字元串值。</span><span class="sxs-lookup"><span data-stu-id="89c0b-116">When the code page of the property set is Unicode, **VT\_LPSTR** string values are converted to Unicode when stored, and back to multibyte string values when retrieved.</span></span>

<span data-ttu-id="89c0b-117">透過呼叫 [**IPropertyStorage：： Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)來設定 **PROPSETFLAG \_ ANSI** 旗標，以反映基礎字碼頁是否為或不是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="89c0b-117">Setting the **PROPSETFLAG\_ANSI** flag as reported through a call to [**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) reflects whether the underlying code page is or is not Unicode.</span></span> <span data-ttu-id="89c0b-118">請注意，您可以明確讀取屬性識別碼1，以學習字碼頁。</span><span class="sxs-lookup"><span data-stu-id="89c0b-118">Be aware that Property ID 1 can be explicitly read to learn the code page.</span></span>

<span data-ttu-id="89c0b-119">您可以透過呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)來存取屬性識別碼1。</span><span class="sxs-lookup"><span data-stu-id="89c0b-119">You can access Property ID 1 through a call to [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).</span></span> <span data-ttu-id="89c0b-120">不過，它是唯讀的，而且可能不會以 [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)進行更新。</span><span class="sxs-lookup"><span data-stu-id="89c0b-120">However, it is read-only, and may not be updated with [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).</span></span> <span data-ttu-id="89c0b-121">此外，它可能不會使用 [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)來刪除。</span><span class="sxs-lookup"><span data-stu-id="89c0b-121">Furthermore, it may not be deleted with [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).</span></span>

 

 




