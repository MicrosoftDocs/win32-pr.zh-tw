---
title: 卸載方法
description: 卸載方法
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682011"
---
# <a name="unload-method"></a><span data-ttu-id="5c3b2-103">卸載方法</span><span class="sxs-lookup"><span data-stu-id="5c3b2-103">Unload Method</span></span>

<span data-ttu-id="5c3b2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5c3b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5c3b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="5c3b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5c3b2-106">卸載指定字元的字元資料。</span><span class="sxs-lookup"><span data-stu-id="5c3b2-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="5c3b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="5c3b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5c3b2-108">*代理程式 ***。字元。 Unload "*** CharacterID \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="5c3b2-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c3b2-109">備註</span><span class="sxs-lookup"><span data-stu-id="5c3b2-109">Remarks</span></span>

<span data-ttu-id="5c3b2-110">當您不再需要字元時，請使用這個方法來釋出用來儲存字元相關資訊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5c3b2-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="5c3b2-111">如果您再次存取此字元，請使用 [**Load**](load-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5c3b2-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="5c3b2-112">這個方法不會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="5c3b2-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 