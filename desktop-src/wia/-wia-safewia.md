---
description: SafeWia 物件是一種 &\# 0034; 可安全的腳本&\# 0034; 所有 Windows 映像取得 (WIA 的進入點) 腳本功能。
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: SafeWia 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970821"
---
# <a name="safewia-object"></a><span data-ttu-id="297bf-103">SafeWia 物件</span><span class="sxs-lookup"><span data-stu-id="297bf-103">SafeWia object</span></span>

<span data-ttu-id="297bf-104">**SafeWia** 物件是所有 Windows 映像取得 (WIA) 腳本功能的「安全的腳本」進入點。</span><span class="sxs-lookup"><span data-stu-id="297bf-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="297bf-105">使用 WIA 腳本模型的任何應用程式都必須建立 **SafeWia** 或 [**WIA**](-wia-wia.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="297bf-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="297bf-106">您可以使用該物件來列舉和建立裝置，並接收硬體事件的通知。</span><span class="sxs-lookup"><span data-stu-id="297bf-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="297bf-107">成員</span><span class="sxs-lookup"><span data-stu-id="297bf-107">Members</span></span>

<span data-ttu-id="297bf-108">**SafeWia** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="297bf-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="297bf-109">方法</span><span class="sxs-lookup"><span data-stu-id="297bf-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="297bf-110">屬性</span><span class="sxs-lookup"><span data-stu-id="297bf-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="297bf-111">方法</span><span class="sxs-lookup"><span data-stu-id="297bf-111">Methods</span></span>

<span data-ttu-id="297bf-112">**SafeWia** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="297bf-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="297bf-113">方法</span><span class="sxs-lookup"><span data-stu-id="297bf-113">Method</span></span>                             | <span data-ttu-id="297bf-114">描述</span><span class="sxs-lookup"><span data-stu-id="297bf-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="297bf-115">**創建**</span><span class="sxs-lookup"><span data-stu-id="297bf-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="297bf-116">[**Wia**](-wia-wia.md)物件的 [**Create**](-wia-iwia-create.md)方法會連接到指定的 Wia 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。</span><span class="sxs-lookup"><span data-stu-id="297bf-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="297bf-117">屬性</span><span class="sxs-lookup"><span data-stu-id="297bf-117">Properties</span></span>

<span data-ttu-id="297bf-118">**SafeWia** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="297bf-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="297bf-119">屬性</span><span class="sxs-lookup"><span data-stu-id="297bf-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="297bf-120">存取類型</span><span class="sxs-lookup"><span data-stu-id="297bf-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="297bf-121">Description</span><span class="sxs-lookup"><span data-stu-id="297bf-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="297bf-122"><a href="-wia-iwia-devices.md"><strong>設備</strong></a></span><span class="sxs-lookup"><span data-stu-id="297bf-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="297bf-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="297bf-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="297bf-124"><a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a>物件的集合，代表安裝在電腦上的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="297bf-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="297bf-125">唯讀。</span><span class="sxs-lookup"><span data-stu-id="297bf-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="297bf-126">這個集合是以0為基礎。</span><span class="sxs-lookup"><span data-stu-id="297bf-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="297bf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="297bf-127">Requirements</span></span>



| <span data-ttu-id="297bf-128">需求</span><span class="sxs-lookup"><span data-stu-id="297bf-128">Requirement</span></span> | <span data-ttu-id="297bf-129">值</span><span class="sxs-lookup"><span data-stu-id="297bf-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="297bf-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="297bf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="297bf-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="297bf-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="297bf-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="297bf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="297bf-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="297bf-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="297bf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="297bf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="297bf-135"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="297bf-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="297bf-136">IID</span><span class="sxs-lookup"><span data-stu-id="297bf-136">IID</span></span><br/>                      | <span data-ttu-id="297bf-137">CLSID \_ SafeWia</span><span class="sxs-lookup"><span data-stu-id="297bf-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="297bf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="297bf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297bf-139">**Wia**</span><span class="sxs-lookup"><span data-stu-id="297bf-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




