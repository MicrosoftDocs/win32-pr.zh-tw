---
description: Windows Installer 可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: 關於屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192478"
---
# <a name="about-properties"></a><span data-ttu-id="60b59-103">關於屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-103">About Properties</span></span>

<span data-ttu-id="60b59-104">Windows Installer 可以使用安裝封裝或使用者所定義的變數值來設定軟體安裝。</span><span class="sxs-lookup"><span data-stu-id="60b59-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="60b59-105">在安裝期間，Windows Installer 會使用三種類別的全域變數：</span><span class="sxs-lookup"><span data-stu-id="60b59-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="60b59-106">私用屬性：安裝程式會在內部使用私用屬性，且其值必須撰寫至安裝資料庫，或設定為作業環境所決定的值。</span><span class="sxs-lookup"><span data-stu-id="60b59-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="60b59-107">公用屬性：公用屬性可以撰寫至資料庫中，並且由使用者或系統管理員在命令列上進行變更，方法是套用轉換，或與撰寫的使用者介面互動。</span><span class="sxs-lookup"><span data-stu-id="60b59-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="60b59-108">受限制的公用屬性：基於安全性目的，安裝套件的作者可以限制使用者可變更的公用屬性。</span><span class="sxs-lookup"><span data-stu-id="60b59-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="60b59-109">並非所有屬性都必須在每個封裝中定義，因此必須在每個封裝中定義一組小型的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="60b59-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="60b59-110">安裝程式會以特定的優先順序順序設定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="60b59-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="60b59-111">私用屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="60b59-112">公用屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="60b59-113">受限制的公用屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="60b59-114">必要屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="60b59-115">屬性優先順序的順序</span><span class="sxs-lookup"><span data-stu-id="60b59-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="60b59-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="60b59-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60b59-117">使用屬性</span><span class="sxs-lookup"><span data-stu-id="60b59-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="60b59-118">屬性參考</span><span class="sxs-lookup"><span data-stu-id="60b59-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



