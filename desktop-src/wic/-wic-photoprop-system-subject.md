---
description: '[System.object] 屬性的相片中繼資料原則。'
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: System. Subject 相片中繼資料原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975211"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="6430d-103">System. Subject 相片中繼資料原則</span><span class="sxs-lookup"><span data-stu-id="6430d-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="6430d-104">[ [System.object](../properties/props-system-subject.md) ] 屬性的相片中繼資料原則。</span><span class="sxs-lookup"><span data-stu-id="6430d-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6430d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6430d-105">PKEY</span></span>

<span data-ttu-id="6430d-106">PKEY \_ 主旨</span><span class="sxs-lookup"><span data-stu-id="6430d-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="6430d-107">容器</span><span class="sxs-lookup"><span data-stu-id="6430d-107">Containers</span></span>

<span data-ttu-id="6430d-108">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="6430d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6430d-109">唯讀</span><span class="sxs-lookup"><span data-stu-id="6430d-109">Read-Only</span></span>

<span data-ttu-id="6430d-110">No</span><span class="sxs-lookup"><span data-stu-id="6430d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6430d-111">輸出 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="6430d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6430d-112">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6430d-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="6430d-113">輸入 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="6430d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="6430d-114">VT \_ LPWSTR 或 vt \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="6430d-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6430d-115">衝突解決原則</span><span class="sxs-lookup"><span data-stu-id="6430d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6430d-116">不同架構的值會進行協調。</span><span class="sxs-lookup"><span data-stu-id="6430d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6430d-117">JPEG 原則</span><span class="sxs-lookup"><span data-stu-id="6430d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6430d-118">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-118">Read Paths</span></span>



| <span data-ttu-id="6430d-119">單</span><span class="sxs-lookup"><span data-stu-id="6430d-119">Order</span></span> | <span data-ttu-id="6430d-120">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-120">Path</span></span>                     | <span data-ttu-id="6430d-121">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6430d-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="6430d-122">1</span><span class="sxs-lookup"><span data-stu-id="6430d-122">1</span></span>     | <span data-ttu-id="6430d-123">/app1/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="6430d-124">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="6430d-124">unicode\_bytes</span></span> |
| <span data-ttu-id="6430d-125">2</span><span class="sxs-lookup"><span data-stu-id="6430d-125">2</span></span>     | <span data-ttu-id="6430d-126">/app1/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="6430d-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="6430d-127">ascii</span><span class="sxs-lookup"><span data-stu-id="6430d-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="6430d-128">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-128">Write Paths</span></span>



| <span data-ttu-id="6430d-129">單</span><span class="sxs-lookup"><span data-stu-id="6430d-129">Order</span></span> | <span data-ttu-id="6430d-130">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-130">Path</span></span>                     | <span data-ttu-id="6430d-131">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6430d-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="6430d-132">1</span><span class="sxs-lookup"><span data-stu-id="6430d-132">1</span></span>     | <span data-ttu-id="6430d-133">/app1/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="6430d-134">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="6430d-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="6430d-135">移除路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-135">Remove Paths</span></span>



| <span data-ttu-id="6430d-136">單</span><span class="sxs-lookup"><span data-stu-id="6430d-136">Order</span></span> | <span data-ttu-id="6430d-137">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6430d-138">1</span><span class="sxs-lookup"><span data-stu-id="6430d-138">1</span></span>     | <span data-ttu-id="6430d-139">/app1/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="6430d-140">2</span><span class="sxs-lookup"><span data-stu-id="6430d-140">2</span></span>     | <span data-ttu-id="6430d-141">/app1/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="6430d-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="6430d-142">TIFF 原則</span><span class="sxs-lookup"><span data-stu-id="6430d-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6430d-143">讀取路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-143">Read Paths</span></span>



| <span data-ttu-id="6430d-144">單</span><span class="sxs-lookup"><span data-stu-id="6430d-144">Order</span></span> | <span data-ttu-id="6430d-145">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-145">Path</span></span>                | <span data-ttu-id="6430d-146">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6430d-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="6430d-147">1</span><span class="sxs-lookup"><span data-stu-id="6430d-147">1</span></span>     | <span data-ttu-id="6430d-148">/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="6430d-149">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="6430d-149">unicode\_bytes</span></span> |
| <span data-ttu-id="6430d-150">2</span><span class="sxs-lookup"><span data-stu-id="6430d-150">2</span></span>     | <span data-ttu-id="6430d-151">/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="6430d-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="6430d-152">ascii</span><span class="sxs-lookup"><span data-stu-id="6430d-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="6430d-153">寫入路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-153">Write Paths</span></span>



| <span data-ttu-id="6430d-154">單</span><span class="sxs-lookup"><span data-stu-id="6430d-154">Order</span></span> | <span data-ttu-id="6430d-155">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-155">Path</span></span>                | <span data-ttu-id="6430d-156">磁片格式</span><span class="sxs-lookup"><span data-stu-id="6430d-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="6430d-157">1</span><span class="sxs-lookup"><span data-stu-id="6430d-157">1</span></span>     | <span data-ttu-id="6430d-158">/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="6430d-159">unicode \_ 位元組</span><span class="sxs-lookup"><span data-stu-id="6430d-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="6430d-160">移除路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-160">Remove Paths</span></span>



| <span data-ttu-id="6430d-161">單</span><span class="sxs-lookup"><span data-stu-id="6430d-161">Order</span></span> | <span data-ttu-id="6430d-162">路徑</span><span class="sxs-lookup"><span data-stu-id="6430d-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="6430d-163">1</span><span class="sxs-lookup"><span data-stu-id="6430d-163">1</span></span>     | <span data-ttu-id="6430d-164">/ifd/{ushort = 40095}</span><span class="sxs-lookup"><span data-stu-id="6430d-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="6430d-165">2</span><span class="sxs-lookup"><span data-stu-id="6430d-165">2</span></span>     | <span data-ttu-id="6430d-166">/ifd/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="6430d-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="6430d-167">備註</span><span class="sxs-lookup"><span data-stu-id="6430d-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6430d-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="6430d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6430d-169">System. Subject</span><span class="sxs-lookup"><span data-stu-id="6430d-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
