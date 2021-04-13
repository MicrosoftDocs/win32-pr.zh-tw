---
title: ExtraData 屬性
description: ExtraData 屬性
ms.assetid: 504fb615-5b99-4023-af26-b5b051a276d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2105e7e981223856d7c0a589f3134fe6dc12792
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300556"
---
# <a name="extradata-property"></a><span data-ttu-id="21f37-103">ExtraData 屬性</span><span class="sxs-lookup"><span data-stu-id="21f37-103">ExtraData Property</span></span>

<span data-ttu-id="21f37-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="21f37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="21f37-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="21f37-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="21f37-106">傳回字串，這個字串會指定儲存為字元一部分的其他資料。</span><span class="sxs-lookup"><span data-stu-id="21f37-106">Returns a string that specifies additional data stored as part of the character.</span></span>

</dd> <dt>

<span data-ttu-id="21f37-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="21f37-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="21f37-108">*代理程式*。**( "***CharacterID***" ) 的字元。ExtraData**</span><span class="sxs-lookup"><span data-stu-id="21f37-108">*agent*.**Characters("***CharacterID***").ExtraData**</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21f37-109">備註</span><span class="sxs-lookup"><span data-stu-id="21f37-109">Remarks</span></span>

<span data-ttu-id="21f37-110">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義字元之 **ExtraData** 屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="21f37-110">The default value for the **ExtraData** property for a character is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="21f37-111">它無法在執行時間變更或指定。</span><span class="sxs-lookup"><span data-stu-id="21f37-111">It cannot be changed or specified at run time.</span></span>

> [!Note]  
> <span data-ttu-id="21f37-112">**ExtraData** 屬性設定為選擇性，而且可能不會提供給所有字元。</span><span class="sxs-lookup"><span data-stu-id="21f37-112">The **ExtraData** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




