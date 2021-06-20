---
title: '已啟用屬性 (AudioOutput 物件) '
description: 瞭解已啟用的 AudioOutput 物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407341"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="41055-104">已啟用屬性 (AudioOutput 物件) </span><span class="sxs-lookup"><span data-stu-id="41055-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="41055-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="41055-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="41055-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="41055-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="41055-107">傳回布林值，指出是否已啟用音訊 (讀出) 輸出。</span><span class="sxs-lookup"><span data-stu-id="41055-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="41055-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="41055-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="41055-109">*代理程式 \* \* *。AudioOutput。已啟用**</span><span class="sxs-lookup"><span data-stu-id="41055-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="41055-110">值</span><span class="sxs-lookup"><span data-stu-id="41055-110">Value</span></span>     | <span data-ttu-id="41055-111">描述</span><span class="sxs-lookup"><span data-stu-id="41055-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="41055-112">**True**</span><span class="sxs-lookup"><span data-stu-id="41055-112">**True**</span></span>  | <span data-ttu-id="41055-113">已啟用 (預設) 的語音輸出。</span><span class="sxs-lookup"><span data-stu-id="41055-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="41055-114">**False**</span><span class="sxs-lookup"><span data-stu-id="41055-114">**False**</span></span> | <span data-ttu-id="41055-115">語音音訊輸出已停用。</span><span class="sxs-lookup"><span data-stu-id="41055-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41055-116">備註</span><span class="sxs-lookup"><span data-stu-id="41055-116">Remarks</span></span>

<span data-ttu-id="41055-117">這個屬性會在 [代理程式] 屬性工作表的 [輸出] 頁面上反映 [播放音訊輸出] 選項， ([Advanced Character Options]) 。</span><span class="sxs-lookup"><span data-stu-id="41055-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="41055-118">當 [**Enabled**](enabled-property.md) 屬性傳回 **True** 時，如果已安裝相容的 TTS 引擎或您使用音效檔來進行語音輸出，則 [**說話**](speak-method.md) 方法會產生音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="41055-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="41055-119">當它傳回 **False** 時，表示語音輸出未安裝或已由使用者停用。</span><span class="sxs-lookup"><span data-stu-id="41055-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="41055-120">屬性設定適用于所有代理程式字元，而且是唯讀的;只有使用者可以設定此屬性值。</span><span class="sxs-lookup"><span data-stu-id="41055-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="41055-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41055-121">See Also</span></span>

[<span data-ttu-id="41055-122">AgentPropertyChange 事件</span><span class="sxs-lookup"><span data-stu-id="41055-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




