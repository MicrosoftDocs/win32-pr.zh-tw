---
description: 正在抓取和設定地區設定資訊
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: 正在抓取和設定地區設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970404"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="dc723-103">正在抓取和設定地區設定資訊</span><span class="sxs-lookup"><span data-stu-id="dc723-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="dc723-104">應用程式必須能夠取得及設定有關可用 [地區設定和語言](locales-and-languages.md)的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="dc723-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="dc723-105">地區設定資訊的每個專案（例如一周的特定一天名稱或作為小數分隔符號的字元）都有對應的常數。</span><span class="sxs-lookup"><span data-stu-id="dc723-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="dc723-106">可用的常數會定義于 [地區設定資訊常數](locale-information-constants.md)中。</span><span class="sxs-lookup"><span data-stu-id="dc723-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="dc723-107">您的應用程式一律會將地區設定資訊儲存並操作為以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="dc723-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="dc723-108">不允許任何二進位資料，而且必須將任何數值指定為文字。</span><span class="sxs-lookup"><span data-stu-id="dc723-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="dc723-109">每種類型的資訊都有特定的格式。</span><span class="sxs-lookup"><span data-stu-id="dc723-109">Each type of information has a particular format.</span></span> <span data-ttu-id="dc723-110">此外，也會將數個型別連結在一起，如此一來，變更一種類型也會變更另一種類型的值。</span><span class="sxs-lookup"><span data-stu-id="dc723-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="dc723-111">為了抓取地區設定資訊，應用程式會以與所需資訊對應的常數來呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 。</span><span class="sxs-lookup"><span data-stu-id="dc723-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="dc723-112">應用程式可以呼叫 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) 來設定地區設定資訊的專案。</span><span class="sxs-lookup"><span data-stu-id="dc723-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="dc723-113">雖然可能會支援 [地區設定識別碼](locale-identifiers.md) ，但它無法供應用程式使用，除非也已安裝對應的地區設定。</span><span class="sxs-lookup"><span data-stu-id="dc723-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="dc723-114">因為大部分的地區設定資訊常數都是互斥的，所以一次只能處理一種類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc723-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="dc723-115">這項規則的例外狀況為 [地區設定 \_ 使用 \_ CP \_ ACP](locale-use-cp-acp.md)、地區設定傳回 [ \_ \_ 編號](locale-return-constants.md)和 [地區設定 \_ NOUSEROVERRIDE](locale-nouseroverride.md)，可以使用二進位或來結合其他常數。</span><span class="sxs-lookup"><span data-stu-id="dc723-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="dc723-116">強烈建議您不要使用地區設定 \_ NOUSEROVERRIDE，因為它會停用使用者喜好設定。</span><span class="sxs-lookup"><span data-stu-id="dc723-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="dc723-117">如同一些應用程式，例如 Microsoft Active Directory，您的應用程式可以在可排序的資料庫中維護其字串。</span><span class="sxs-lookup"><span data-stu-id="dc723-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="dc723-118">如需詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="dc723-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc723-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc723-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc723-120">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="dc723-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="dc723-121">地區設定資訊常數</span><span class="sxs-lookup"><span data-stu-id="dc723-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="dc723-122">處理應用程式中的排序</span><span class="sxs-lookup"><span data-stu-id="dc723-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="dc723-123">使用自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="dc723-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 



