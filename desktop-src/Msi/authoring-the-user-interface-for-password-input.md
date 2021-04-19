---
description: 針對每個必須由使用者輸入的密碼，在儲存密碼值的對話方塊上新增編輯控制項至屬性。
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: 撰寫密碼輸入的消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971752"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="ebe06-103">撰寫密碼輸入的消費者介面</span><span class="sxs-lookup"><span data-stu-id="ebe06-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="ebe06-104">針對每個必須由使用者輸入的密碼，在儲存密碼值的對話方塊上新增編輯控制項至屬性。</span><span class="sxs-lookup"><span data-stu-id="ebe06-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="ebe06-105">此 [編輯控制項](edit-control.md) 應具有 [密碼控制項屬性](password-control-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="ebe06-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="ebe06-106">這會指定輸入的屬性為密碼，並防止安裝程式將屬性寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="ebe06-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="ebe06-107">密碼編輯控制項的 [控制項屬性](control-attributes.md) 為 MsidbControlAttributesVisible、MsidbControlAttributesEnabled 和 msidbControlAttributesPasswordInput (1 + 2 + 2097152) 。</span><span class="sxs-lookup"><span data-stu-id="ebe06-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="ebe06-108">X、Y、寬度、高度和控制項 \_ 下一步取決於對話方塊上控制項的版面配置。</span><span class="sxs-lookup"><span data-stu-id="ebe06-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="ebe06-109">控制資料表</span><span class="sxs-lookup"><span data-stu-id="ebe06-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="ebe06-110">對話\_</span><span class="sxs-lookup"><span data-stu-id="ebe06-110">Dialog\_</span></span> | <span data-ttu-id="ebe06-111">控制項\_</span><span class="sxs-lookup"><span data-stu-id="ebe06-111">Control\_</span></span>            | <span data-ttu-id="ebe06-112">類型</span><span class="sxs-lookup"><span data-stu-id="ebe06-112">Type</span></span> | <span data-ttu-id="ebe06-113">X</span><span class="sxs-lookup"><span data-stu-id="ebe06-113">X</span></span>   | <span data-ttu-id="ebe06-114">Y</span><span class="sxs-lookup"><span data-stu-id="ebe06-114">Y</span></span>   | <span data-ttu-id="ebe06-115">寬度</span><span class="sxs-lookup"><span data-stu-id="ebe06-115">Width</span></span> | <span data-ttu-id="ebe06-116">高度</span><span class="sxs-lookup"><span data-stu-id="ebe06-116">Height</span></span> | <span data-ttu-id="ebe06-117">屬性</span><span class="sxs-lookup"><span data-stu-id="ebe06-117">Attributes</span></span> | <span data-ttu-id="ebe06-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ebe06-118">Property</span></span>         | <span data-ttu-id="ebe06-119">Text</span><span class="sxs-lookup"><span data-stu-id="ebe06-119">Text</span></span> | <span data-ttu-id="ebe06-120">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="ebe06-120">Control\_Next</span></span> | <span data-ttu-id="ebe06-121">Help</span><span class="sxs-lookup"><span data-stu-id="ebe06-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="ebe06-122">MyDialog</span><span class="sxs-lookup"><span data-stu-id="ebe06-122">MyDialog</span></span> | <span data-ttu-id="ebe06-123">TestUserPasswordEdit</span><span class="sxs-lookup"><span data-stu-id="ebe06-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="ebe06-124">編輯</span><span class="sxs-lookup"><span data-stu-id="ebe06-124">Edit</span></span> | <span data-ttu-id="ebe06-125">25</span><span class="sxs-lookup"><span data-stu-id="ebe06-125">25</span></span>  | <span data-ttu-id="ebe06-126">120</span><span class="sxs-lookup"><span data-stu-id="ebe06-126">120</span></span> | <span data-ttu-id="ebe06-127">300</span><span class="sxs-lookup"><span data-stu-id="ebe06-127">300</span></span>   | <span data-ttu-id="ebe06-128">20</span><span class="sxs-lookup"><span data-stu-id="ebe06-128">20</span></span>     | <span data-ttu-id="ebe06-129">2097155</span><span class="sxs-lookup"><span data-stu-id="ebe06-129">2097155</span></span>    | <span data-ttu-id="ebe06-130">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="ebe06-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="ebe06-131">取消</span><span class="sxs-lookup"><span data-stu-id="ebe06-131">Cancel</span></span>        |      |



 

<span data-ttu-id="ebe06-132">繼續 [保護安裝的安全](securing-the-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="ebe06-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



