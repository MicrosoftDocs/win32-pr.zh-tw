---
title: RequestMediaAccessRights 方法
description: RequestMediaAccessRights 方法會要求存取程式庫的指定層級。 |RequestMediaAccessRights 方法
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- requestMediaAccessRights 方法 Windows Media Player
- requestMediaAccessRights 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，requestMediaAccessRights 方法
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994262"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="5bb23-107">RequestMediaAccessRights 方法</span><span class="sxs-lookup"><span data-stu-id="5bb23-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="5bb23-108">**RequestMediaAccessRights** 方法會要求存取程式庫的指定層級。</span><span class="sxs-lookup"><span data-stu-id="5bb23-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb23-109">語法</span><span class="sxs-lookup"><span data-stu-id="5bb23-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="5bb23-110">參數</span><span class="sxs-lookup"><span data-stu-id="5bb23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb23-111">*存取* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bb23-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb23-112">**字串** ，指定所需的存取權限層級。</span><span class="sxs-lookup"><span data-stu-id="5bb23-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="5bb23-113">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5bb23-113">Contains one of the following values.</span></span>



| <span data-ttu-id="5bb23-114">String</span><span class="sxs-lookup"><span data-stu-id="5bb23-114">String</span></span> | <span data-ttu-id="5bb23-115">Description</span><span class="sxs-lookup"><span data-stu-id="5bb23-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="5bb23-116">無</span><span class="sxs-lookup"><span data-stu-id="5bb23-116">none</span></span>   | <span data-ttu-id="5bb23-117">僅限目前的專案存取權限。</span><span class="sxs-lookup"><span data-stu-id="5bb23-117">Current item access rights only.</span></span> |
| <span data-ttu-id="5bb23-118">讀取</span><span class="sxs-lookup"><span data-stu-id="5bb23-118">read</span></span>   | <span data-ttu-id="5bb23-119">僅限讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="5bb23-119">Read access rights only.</span></span>         |
| <span data-ttu-id="5bb23-120">完整</span><span class="sxs-lookup"><span data-stu-id="5bb23-120">full</span></span>   | <span data-ttu-id="5bb23-121">讀取/寫入存取權限。</span><span class="sxs-lookup"><span data-stu-id="5bb23-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb23-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bb23-122">Return value</span></span>

<span data-ttu-id="5bb23-123">這個方法會傳回 **布林** 值，指出是否已授與要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="5bb23-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb23-124">備註</span><span class="sxs-lookup"><span data-stu-id="5bb23-124">Remarks</span></span>

<span data-ttu-id="5bb23-125">網頁必須先向使用者要求許可權，以讀取或寫入文件庫中的資料。</span><span class="sxs-lookup"><span data-stu-id="5bb23-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="5bb23-126">叫用這個方法會提示使用者一個對話方塊，要求指定的許可權等級。</span><span class="sxs-lookup"><span data-stu-id="5bb23-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="5bb23-127">這表示，如果未授與適當的存取權限，就無法從程式碼存取某些方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="5bb23-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="5bb23-128">您可以使用 *設定* 來抓取目前的存取權限層級。**mediaAccessRights**。</span><span class="sxs-lookup"><span data-stu-id="5bb23-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="5bb23-129">**Windows Media Player 10** 行動裝置版：此方法一律會傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="5bb23-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb23-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bb23-130">Requirements</span></span>



| <span data-ttu-id="5bb23-131">需求</span><span class="sxs-lookup"><span data-stu-id="5bb23-131">Requirement</span></span> | <span data-ttu-id="5bb23-132">值</span><span class="sxs-lookup"><span data-stu-id="5bb23-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb23-133">版本</span><span class="sxs-lookup"><span data-stu-id="5bb23-133">Version</span></span><br/> | <span data-ttu-id="5bb23-134">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="5bb23-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5bb23-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5bb23-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="5bb23-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bb23-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb23-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bb23-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb23-138">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="5bb23-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="5bb23-139">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5bb23-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





