---
description: 下列章節說明如何使用內建的安裝程式屬性，以及封裝作者所定義的其他屬性。
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: 使用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113244"
---
# <a name="using-properties"></a><span data-ttu-id="db992-103">使用屬性</span><span class="sxs-lookup"><span data-stu-id="db992-103">Using Properties</span></span>

<span data-ttu-id="db992-104">下列章節說明如何使用內建的安裝程式屬性，以及封裝作者所定義的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="db992-104">The following sections describe using the built-in installer properties and additional properties defined by the package author.</span></span> <span data-ttu-id="db992-105">屬性可以是 [公用屬性](public-properties.md) 或 [私用屬性](private-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="db992-105">Properties can be either [public properties](public-properties.md) or [private properties](private-properties.md).</span></span> <span data-ttu-id="db992-106">在初始化安裝程式時需要定義的每個屬性，都必須具有 [屬性工作表](property-table.md)中列出的名稱和初始值。</span><span class="sxs-lookup"><span data-stu-id="db992-106">Every property that needs to be defined upon initialization of the installer must have its name and initial value listed in the [Property table](property-table.md).</span></span> <span data-ttu-id="db992-107">具有 Null 值的屬性不會列在屬性工作表中。</span><span class="sxs-lookup"><span data-stu-id="db992-107">Properties having a Null value are not listed in the Property table.</span></span> <span data-ttu-id="db992-108">您可以從程式和自訂動作取得或設定屬性，並從命令列設定公用屬性。</span><span class="sxs-lookup"><span data-stu-id="db992-108">You can get or set properties from programs and custom actions and set public properties from the command line.</span></span> <span data-ttu-id="db992-109">您可以使用條件陳述式中的屬性來修改安裝程式。</span><span class="sxs-lookup"><span data-stu-id="db992-109">The installation process can be modified by using properties in conditional statements.</span></span>

[<span data-ttu-id="db992-110">屬性名稱的限制</span><span class="sxs-lookup"><span data-stu-id="db992-110">Restrictions on Property Names</span></span>](restrictions-on-property-names.md)

[<span data-ttu-id="db992-111">屬性值的初始化</span><span class="sxs-lookup"><span data-stu-id="db992-111">Initialization of Property Values</span></span>](initialization-of-property-values.md)

[<span data-ttu-id="db992-112">取得和設定屬性</span><span class="sxs-lookup"><span data-stu-id="db992-112">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)

[<span data-ttu-id="db992-113">在條件陳述式中使用屬性</span><span class="sxs-lookup"><span data-stu-id="db992-113">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)

[<span data-ttu-id="db992-114">使用路徑中的目錄屬性</span><span class="sxs-lookup"><span data-stu-id="db992-114">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)

> [!Note]  
> <span data-ttu-id="db992-115">請勿將屬性用於密碼或其他必須保持安全的資訊。</span><span class="sxs-lookup"><span data-stu-id="db992-115">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="db992-116">安裝程式可能會將撰寫的屬性值寫入至屬性工作表，或在執行時間建立至記錄檔或系統登錄。</span><span class="sxs-lookup"><span data-stu-id="db992-116">The installer may write the value of a property authored into the Property table or created at runtime into a log or the system registry.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="db992-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="db992-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db992-118">關於屬性</span><span class="sxs-lookup"><span data-stu-id="db992-118">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="db992-119">屬性參考</span><span class="sxs-lookup"><span data-stu-id="db992-119">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



