---
description: AVAILABLEFREEREG 屬性會在呼叫 AllocateRegistrySpace 動作之後，以 kb 為單位指定登錄中的可用空間總計（以 kb 為單位）。AVAILABLEFREEREG 屬性的最大值為 2000000 kb。這個屬性只會在 Windows 2000 上設定。
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: AVAILABLEFREEREG 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980132"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="9ff96-103">AVAILABLEFREEREG 屬性</span><span class="sxs-lookup"><span data-stu-id="9ff96-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="9ff96-104">**AVAILABLEFREEREG** 屬性會在呼叫 [AllocateRegistrySpace 動作](allocateregistryspace-action.md)之後，以 kb 為單位指定登錄中的可用空間總計（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ff96-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="9ff96-105">**AVAILABLEFREEREG** 屬性的最大值為 2000000 kb。</span><span class="sxs-lookup"><span data-stu-id="9ff96-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="9ff96-106">這個屬性只會在 Windows 2000 上設定。</span><span class="sxs-lookup"><span data-stu-id="9ff96-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff96-107">備註</span><span class="sxs-lookup"><span data-stu-id="9ff96-107">Remarks</span></span>

<span data-ttu-id="9ff96-108">**AVAILABLEFREEREG** 屬性必須設定為夠大的值，以確保登錄中的足夠空間可供安裝所加入的所有註冊資訊使用。</span><span class="sxs-lookup"><span data-stu-id="9ff96-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="9ff96-109">確保足夠空間所需的最小值取決於 [AllocateRegistrySpace 動作](allocateregistryspace-action.md) 在動作順序中的 [位置，因為](registry-table.md)安裝程式會在登錄、 [類別](class-table.md)、 [SelfReg](selfreg-table.md)、 [延伸](extension-table.md)模組、 [MIME](mime-table.md)和 [動詞](verb-table.md) 資料表中註冊資訊時，自動增加所需的空間。</span><span class="sxs-lookup"><span data-stu-id="9ff96-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="9ff96-110">安裝程式不會將登錄空間總數增加至 **AVAILABLEFREEREG** 所指定的數量，直到達到動作順序中的 AllocateRegistrySpace 為止。</span><span class="sxs-lookup"><span data-stu-id="9ff96-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="9ff96-111">如果 AllocateRegistrySpace 是動作順序中的第一個動作，則應該將 **AVAILABLEFREEREG** 設定為登錄資料表、類別資料表、TypeLib 資料表、SelfReg 資料表、延伸模組資料表、MIME 資料表、動詞資料表、 [自訂動作](custom-actions.md) 註冊、自我註冊，以及安裝期間所寫入的任何其他登錄資訊所需的總空間。</span><span class="sxs-lookup"><span data-stu-id="9ff96-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="9ff96-112">**AVAILABLEFREEREG** 的值是安裝所加入的總資訊量，可確保所有情況下都有足夠的空間。</span><span class="sxs-lookup"><span data-stu-id="9ff96-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="9ff96-113">這也是最常見的情況。</span><span class="sxs-lookup"><span data-stu-id="9ff96-113">This is also the most common case.</span></span>

<span data-ttu-id="9ff96-114">如果 AllocateRegistrySpace 動作可以在寫入註冊資料的所有 [標準動作](standard-actions.md) （例如 [WriteRegistryValues](writeregistryvalues-action.md) 和 [RegisterClassInfo](registerclassinfo-action.md)）之後，于動作順序中撰寫，則 **AVAILABLEFREEREG** 需求的值只會設定為註冊自訂動作、註冊類型程式庫，以及尚未透過資料表註冊之任何其他資訊的必要空間。</span><span class="sxs-lookup"><span data-stu-id="9ff96-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff96-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ff96-115">Requirements</span></span>



| <span data-ttu-id="9ff96-116">需求</span><span class="sxs-lookup"><span data-stu-id="9ff96-116">Requirement</span></span> | <span data-ttu-id="9ff96-117">值</span><span class="sxs-lookup"><span data-stu-id="9ff96-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff96-118">版本</span><span class="sxs-lookup"><span data-stu-id="9ff96-118">Version</span></span><br/> | <span data-ttu-id="9ff96-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9ff96-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ff96-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9ff96-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ff96-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="9ff96-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9ff96-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ff96-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ff96-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ff96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff96-124">屬性</span><span class="sxs-lookup"><span data-stu-id="9ff96-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




