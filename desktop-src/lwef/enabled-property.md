---
title: 'Enabled 屬性 (Balloon 物件) '
description: Enabled 屬性
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "107001289"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="cba96-103">Enabled 屬性 (Balloon 物件) </span><span class="sxs-lookup"><span data-stu-id="cba96-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="cba96-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="cba96-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cba96-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="cba96-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cba96-106">傳回是否針對指定的字元啟用文字批註。</span><span class="sxs-lookup"><span data-stu-id="cba96-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="cba96-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="cba96-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cba96-108">\*代理程式 \***。 ( "**_CharacterID_*_" ) 的字元。氣球。已啟用_*</span><span class="sxs-lookup"><span data-stu-id="cba96-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="cba96-109">值</span><span class="sxs-lookup"><span data-stu-id="cba96-109">Value</span></span>     | <span data-ttu-id="cba96-110">描述</span><span class="sxs-lookup"><span data-stu-id="cba96-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="cba96-111">**True**</span><span class="sxs-lookup"><span data-stu-id="cba96-111">**True**</span></span>  | <span data-ttu-id="cba96-112">批註提示已啟用。</span><span class="sxs-lookup"><span data-stu-id="cba96-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="cba96-113">**False**</span><span class="sxs-lookup"><span data-stu-id="cba96-113">**False**</span></span> | <span data-ttu-id="cba96-114">批註提示已停用。</span><span class="sxs-lookup"><span data-stu-id="cba96-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cba96-115">備註</span><span class="sxs-lookup"><span data-stu-id="cba96-115">Remarks</span></span>

<span data-ttu-id="cba96-116">**Enabled** 屬性會傳回布林值，指定是否啟用氣球。</span><span class="sxs-lookup"><span data-stu-id="cba96-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="cba96-117">當字元在 Microsoft Agent 字元編輯器中進行編譯時，會將文字氣球預設狀態設定為字元定義的一部分。</span><span class="sxs-lookup"><span data-stu-id="cba96-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="cba96-118">如果將字元定義為不支援文字提示字元，則字元的這個屬性一律會是 **False** 。</span><span class="sxs-lookup"><span data-stu-id="cba96-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




