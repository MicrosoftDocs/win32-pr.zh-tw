---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: 條件約束和 PrintTicket 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945740"
---
# <a name="constraints-and-printticket-validation"></a><span data-ttu-id="3bbea-104">條件約束和 PrintTicket 驗證</span><span class="sxs-lookup"><span data-stu-id="3bbea-104">Constraints and PrintTicket Validation</span></span>

<span data-ttu-id="3bbea-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="3bbea-105">This topic is not current.</span></span> <span data-ttu-id="3bbea-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="3bbea-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3bbea-107">如 PrintCapabilities 架構一節中所述，PrintCapabilities 檔中表示的一些可能設定結果對裝置而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="3bbea-107">As discussed in the PrintCapabilities Schema section, some of the possible configuration outcomes expressed in a PrintCapabilities document are invalid for the device.</span></span> <span data-ttu-id="3bbea-108">不正確設定會被視為包含 (在) 的 PPD/GPD 檔案領域中的條件約束衝突。</span><span class="sxs-lookup"><span data-stu-id="3bbea-108">Configurations that are invalid are said to contain constraint conflicts (a term used in the world of PPD/GPD files).</span></span> <span data-ttu-id="3bbea-109">為了避免條件約束衝突，PrintTicket 提供者必須支援 PrintTicket 驗證作業，用戶端會使用該作業來對其 PrintTicket 執行驗證。</span><span class="sxs-lookup"><span data-stu-id="3bbea-109">In order to prevent constraint conflicts, PrintTicket providers must support a PrintTicket validation operation that clients use to perform validation on their PrintTicket.</span></span> <span data-ttu-id="3bbea-110">此作業應該會偵測指定的設定是否可以在裝置上進行。</span><span class="sxs-lookup"><span data-stu-id="3bbea-110">This operation should detect whether the specified configuration can occur on the device.</span></span> <span data-ttu-id="3bbea-111">如果無法進行設定 (因為指定的功能和選項元素不存在於目前的裝置中，或因為設定受限制) ，所以作業應修改輸入 PrintTicket，使其包含有效且不受限制的設定。</span><span class="sxs-lookup"><span data-stu-id="3bbea-111">If the configuration cannot occur (because the Feature and Option elements specified do not exist in the current device, or because the configuration is constrained), the operation should modify the input PrintTicket so that it contains valid, unconstrained settings.</span></span> <span data-ttu-id="3bbea-112">作業可能也會移除或驗證 PrintTicket 中的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3bbea-112">The operation might remove or validate other information in the PrintTicket as well.</span></span> <span data-ttu-id="3bbea-113">請注意，遇到條件約束衝突時，驗證程式代碼必須變更其中一個裝置屬性的設定，以避免條件約束衝突。</span><span class="sxs-lookup"><span data-stu-id="3bbea-113">Note that when a constraint conflict is encountered, the validation code must change the setting of one of the device attributes in order to avoid the constraint conflict.</span></span> <span data-ttu-id="3bbea-114">[選項定義](option-definitions.md) 會建議應使用設備磁碟機定義評分程式來判斷應變更哪個裝置屬性，以最妥善地保留使用者的原始意圖。</span><span class="sxs-lookup"><span data-stu-id="3bbea-114">[Option Definitions](option-definitions.md) suggests that a device driver defined scoring process should be used to determine which device attribute should be changed in order to best preserve the user's original intent.</span></span> <span data-ttu-id="3bbea-115">驗證程式代碼可能會將評分程式硬式編碼，以優先使用某個裝置屬性，或使用 PrintTicket 中特定屬性實例所提供的資訊來引導解析度。</span><span class="sxs-lookup"><span data-stu-id="3bbea-115">The validation code might hardcode the scoring process to favor one device attribute over another, or it might use information supplied by a particular Property instance in the PrintTicket to guide resolution.</span></span> <span data-ttu-id="3bbea-116">由於列印架構關鍵字中未定義任何屬性，因此用戶端可以指定每個裝置屬性的相對優先權，因此其他 PrintTicket 提供者可能會忽略用於此用途的任何私用 PrintTicket 屬性元素。</span><span class="sxs-lookup"><span data-stu-id="3bbea-116">Because there is no Property defined in the Print Schema Keywords that allows clients to specify the relative priority of each device attribute, any private PrintTicket Property elements used for this purpose are likely to be ignored by other PrintTicket providers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bbea-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3bbea-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bbea-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="3bbea-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



