---
title: 設定. mediaAccessRights
description: MediaAccessRights 屬性會取得值，指出目前授與存取程式庫的許可權。
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- 設定. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987092"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="a5262-104">設定. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="a5262-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="a5262-105">**MediaAccessRights** 屬性會取得值，指出目前授與存取程式庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="a5262-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5262-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5262-106">Syntax</span></span>

<span data-ttu-id="a5262-107">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="a5262-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="a5262-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="a5262-108">Possible Values</span></span>

<span data-ttu-id="a5262-109">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="a5262-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="a5262-110">值</span><span class="sxs-lookup"><span data-stu-id="a5262-110">Value</span></span> | <span data-ttu-id="a5262-111">描述</span><span class="sxs-lookup"><span data-stu-id="a5262-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="a5262-112">無</span><span class="sxs-lookup"><span data-stu-id="a5262-112">none</span></span>  | <span data-ttu-id="a5262-113">僅限目前的專案存取權限。</span><span class="sxs-lookup"><span data-stu-id="a5262-113">Current item access rights only.</span></span> |
| <span data-ttu-id="a5262-114">讀取</span><span class="sxs-lookup"><span data-stu-id="a5262-114">read</span></span>  | <span data-ttu-id="a5262-115">僅限讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="a5262-115">Read access rights only.</span></span>         |
| <span data-ttu-id="a5262-116">完整</span><span class="sxs-lookup"><span data-stu-id="a5262-116">full</span></span>  | <span data-ttu-id="a5262-117">讀取/寫入存取權限。</span><span class="sxs-lookup"><span data-stu-id="a5262-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="a5262-118">備註</span><span class="sxs-lookup"><span data-stu-id="a5262-118">Remarks</span></span>

<span data-ttu-id="a5262-119">網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="a5262-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="a5262-120">這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="a5262-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="a5262-121">若要取得存取權限，應用程式會呼叫 *設定*。**requestMediaAccessRights**，傳遞指定所需存取權限層級的參數。</span><span class="sxs-lookup"><span data-stu-id="a5262-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="a5262-122">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 **full**。</span><span class="sxs-lookup"><span data-stu-id="a5262-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5262-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5262-123">Requirements</span></span>



| <span data-ttu-id="a5262-124">需求</span><span class="sxs-lookup"><span data-stu-id="a5262-124">Requirement</span></span> | <span data-ttu-id="a5262-125">值</span><span class="sxs-lookup"><span data-stu-id="a5262-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5262-126">版本</span><span class="sxs-lookup"><span data-stu-id="a5262-126">Version</span></span><br/> | <span data-ttu-id="a5262-127">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="a5262-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a5262-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a5262-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="a5262-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5262-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5262-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5262-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5262-131">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="a5262-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="a5262-132">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a5262-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





