---
title: 'Enabled 屬性 (Command 物件) '
description: Enabled 屬性
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968320"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="a66e8-103">Enabled 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="a66e8-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="a66e8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a66e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a66e8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a66e8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a66e8-106">傳回或設定是否在指定的字元快顯功能表中啟用 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="a66e8-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="a66e8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a66e8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a66e8-108">\*代理程式 \***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_\*_"。啟用_ 的 \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="a66e8-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="a66e8-109">部分</span><span class="sxs-lookup"><span data-stu-id="a66e8-109">Part</span></span>      | <span data-ttu-id="a66e8-110">描述</span><span class="sxs-lookup"><span data-stu-id="a66e8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a66e8-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="a66e8-111">*boolean*</span></span> | <span data-ttu-id="a66e8-112">指定是否啟用 **命令** 的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="a66e8-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="a66e8-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="a66e8-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="a66e8-114">**命令** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="a66e8-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="a66e8-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="a66e8-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="a66e8-116">此 **命令** 已停用。</span><span class="sxs-lookup"><span data-stu-id="a66e8-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a66e8-117">備註</span><span class="sxs-lookup"><span data-stu-id="a66e8-117">Remarks</span></span>

<span data-ttu-id="a66e8-118">如果 [ [**已啟用**](enabled-property.md) ] 屬性設定為 [ **True**]，當用戶端應用程式為輸入-主動時， [**命令**](/windows/desktop/lwef/the-command-object) 物件的標題會顯示為字元快顯功能表中的一般文字。</span><span class="sxs-lookup"><span data-stu-id="a66e8-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="a66e8-119">如果 **Enabled** 屬性為 **False**，標題會顯示為無法使用 (已停用) 文字。</span><span class="sxs-lookup"><span data-stu-id="a66e8-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="a66e8-120">語音輸入也無法存取已停用的 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="a66e8-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

