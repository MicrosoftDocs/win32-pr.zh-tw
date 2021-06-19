---
title: 'Enabled 屬性 (Command 物件) '
description: 瞭解已啟用的命令物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407331"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="819db-104">Enabled 屬性 (Command 物件) </span><span class="sxs-lookup"><span data-stu-id="819db-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="819db-105">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="819db-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="819db-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="819db-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="819db-107">傳回或設定是否在指定的字元快顯功能表中啟用 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="819db-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="819db-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="819db-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="819db-109">\*代理程式 \***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_\*_"。啟用_ 的 \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="819db-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="819db-110">部分</span><span class="sxs-lookup"><span data-stu-id="819db-110">Part</span></span>      | <span data-ttu-id="819db-111">描述</span><span class="sxs-lookup"><span data-stu-id="819db-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="819db-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="819db-112">*boolean*</span></span> | <span data-ttu-id="819db-113">指定是否啟用 **命令** 的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="819db-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="819db-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="819db-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="819db-115">**命令** 已啟用。</span><span class="sxs-lookup"><span data-stu-id="819db-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="819db-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="819db-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="819db-117">此 **命令** 已停用。</span><span class="sxs-lookup"><span data-stu-id="819db-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="819db-118">備註</span><span class="sxs-lookup"><span data-stu-id="819db-118">Remarks</span></span>

<span data-ttu-id="819db-119">如果 [ [**已啟用**](enabled-property.md) ] 屬性設定為 [ **True**]，當用戶端應用程式為輸入-主動時， [**命令**](/windows/desktop/lwef/the-command-object) 物件的標題會顯示為字元快顯功能表中的一般文字。</span><span class="sxs-lookup"><span data-stu-id="819db-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="819db-120">如果 **Enabled** 屬性為 **False**，標題會顯示為無法使用 (已停用) 文字。</span><span class="sxs-lookup"><span data-stu-id="819db-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="819db-121">語音輸入也無法存取已停用的 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="819db-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

