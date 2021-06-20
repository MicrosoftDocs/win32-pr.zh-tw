---
title: '啟用的屬性 (語音輸入物件) '
description: 瞭解已啟用的語音輸入物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: d48f02f1-7d93-4780-88a7-61597672bb58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a3e5d7989da4144805fbb926f744026033638d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407321"
---
# <a name="enabled-property-speech-input-object"></a><span data-ttu-id="3d90e-104">啟用的屬性 (語音輸入物件) </span><span class="sxs-lookup"><span data-stu-id="3d90e-104">Enabled Property (Speech Input Object)</span></span>

<span data-ttu-id="3d90e-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3d90e-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3d90e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="3d90e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3d90e-107">傳回布林值，指出是否已啟用語音輸入。</span><span class="sxs-lookup"><span data-stu-id="3d90e-107">Returns a Boolean value indicating whether speech input is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3d90e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3d90e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3d90e-109">*代理程式 \* \* *。SpeechInput。已啟用**</span><span class="sxs-lookup"><span data-stu-id="3d90e-109">*agent\*\*\*.SpeechInput.Enabled*\*</span></span>



| <span data-ttu-id="3d90e-110">值</span><span class="sxs-lookup"><span data-stu-id="3d90e-110">Value</span></span>     | <span data-ttu-id="3d90e-111">描述</span><span class="sxs-lookup"><span data-stu-id="3d90e-111">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="3d90e-112">**True**</span><span class="sxs-lookup"><span data-stu-id="3d90e-112">**True**</span></span>  | <span data-ttu-id="3d90e-113">語音輸入已啟用。</span><span class="sxs-lookup"><span data-stu-id="3d90e-113">Speech input is enabled.</span></span>  |
| <span data-ttu-id="3d90e-114">**False**</span><span class="sxs-lookup"><span data-stu-id="3d90e-114">**False**</span></span> | <span data-ttu-id="3d90e-115">語音輸入已停用。</span><span class="sxs-lookup"><span data-stu-id="3d90e-115">Speech input is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d90e-116">備註</span><span class="sxs-lookup"><span data-stu-id="3d90e-116">Remarks</span></span>

<span data-ttu-id="3d90e-117">[ [**已啟用**](enabled-property.md) ] 屬性會反映 [代理程式] 屬性工作表的 [語音輸入] 頁面上的 [接聽輸入] 選項的字元， ([Advanced Character Options]) 。</span><span class="sxs-lookup"><span data-stu-id="3d90e-117">The [**Enabled**](enabled-property.md) property reflects the Characters Listen For Input option on the Speech Input page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="3d90e-118">屬性設定會影響所有的代理程式字元，而且是唯讀的;只有使用者可以變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="3d90e-118">The property setting affects all Agent characters and is read-only; only the user can change this property.</span></span>

 

 




