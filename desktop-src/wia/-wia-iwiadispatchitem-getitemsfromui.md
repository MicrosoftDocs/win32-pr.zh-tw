---
description: Item 物件的 GetItemsFromUI 方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: GetItemsFromUI 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113904"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="47845-103">GetItemsFromUI 方法</span><span class="sxs-lookup"><span data-stu-id="47845-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="47845-104">[**Item**](-wia-item.md)物件的 **GetItemsFromUI** 方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。</span><span class="sxs-lookup"><span data-stu-id="47845-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="47845-105">語法</span><span class="sxs-lookup"><span data-stu-id="47845-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="47845-106">參數</span><span class="sxs-lookup"><span data-stu-id="47845-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47845-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="47845-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47845-108">類型： **[ **WiaFlag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="47845-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="47845-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="47845-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="47845-110">預設值。</span><span class="sxs-lookup"><span data-stu-id="47845-110">Default.</span></span> <span data-ttu-id="47845-111">\[在中， \] 指定對話方塊的行為。</span><span class="sxs-lookup"><span data-stu-id="47845-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="47845-112">這個參數的有效值與 [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)方法之 *lFlags* 參數的值相同。</span><span class="sxs-lookup"><span data-stu-id="47845-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="47845-113">*意圖* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47845-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47845-114">類型： **WiaIntent**</span><span class="sxs-lookup"><span data-stu-id="47845-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="47845-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="47845-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="47845-116">預設值。</span><span class="sxs-lookup"><span data-stu-id="47845-116">Default.</span></span> <span data-ttu-id="47845-117">\[中的 \] 指定影像所要代表的資料類型。</span><span class="sxs-lookup"><span data-stu-id="47845-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="47845-118">如需影像意圖值的清單，請參閱 [**影像意圖常數**](-wia-imageintentconstants.md)。</span><span class="sxs-lookup"><span data-stu-id="47845-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47845-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="47845-119">Return value</span></span>

<span data-ttu-id="47845-120">類型： **ICollection**</span><span class="sxs-lookup"><span data-stu-id="47845-120">Type: **ICollection**</span></span>

<span data-ttu-id="47845-121">這個方法會傳回代表使用者選取之專案的 [**專案**](-wia-item.md) 物件集合。</span><span class="sxs-lookup"><span data-stu-id="47845-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="47845-122">如果未選取任何專案，則集合是空的。</span><span class="sxs-lookup"><span data-stu-id="47845-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="47845-123">備註</span><span class="sxs-lookup"><span data-stu-id="47845-123">Remarks</span></span>

<span data-ttu-id="47845-124">若為 Microsoft Visual Basic 的應用程式，請新增「Windows 映像取得1.01 類型程式庫」的參考。</span><span class="sxs-lookup"><span data-stu-id="47845-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="47845-125">此方法僅適用于)  (根專案的裝置。</span><span class="sxs-lookup"><span data-stu-id="47845-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="47845-126">方法會傳回代表使用者選取之影像或音訊剪輯的 [**專案**](-wia-item.md) 物件集合。</span><span class="sxs-lookup"><span data-stu-id="47845-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="47845-127">如果使用者未選取任何專案，則方法會傳回空集合。</span><span class="sxs-lookup"><span data-stu-id="47845-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="47845-128">範例</span><span class="sxs-lookup"><span data-stu-id="47845-128">Examples</span></span>

<span data-ttu-id="47845-129">下列範例示範如何使用 **GetItemsFromUI** 方法，以允許使用者從對話方塊中選取影像。</span><span class="sxs-lookup"><span data-stu-id="47845-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="47845-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="47845-130">Requirements</span></span>



| <span data-ttu-id="47845-131">需求</span><span class="sxs-lookup"><span data-stu-id="47845-131">Requirement</span></span> | <span data-ttu-id="47845-132">值</span><span class="sxs-lookup"><span data-stu-id="47845-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47845-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47845-133">Minimum supported client</span></span><br/> | <span data-ttu-id="47845-134">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47845-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47845-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47845-135">Minimum supported server</span></span><br/> | <span data-ttu-id="47845-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47845-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="47845-137">DLL</span><span class="sxs-lookup"><span data-stu-id="47845-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47845-138"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="47845-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




