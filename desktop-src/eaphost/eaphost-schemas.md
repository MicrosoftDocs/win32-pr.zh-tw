---
title: EAPHost 和舊版架構
description: 描述用於建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104373999"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="b5b3e-103">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b5b3e-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="b5b3e-104">本主題說明用來建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="b5b3e-105">關於 EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b5b3e-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="b5b3e-106">建立具有 [eaphostconfig](eaphostconfigschema-schema.md) 架構的設定 XML建立具有 [eaphostusercredentials](eaphostusercredentialsschema-schema.md) 架構的認證 XML。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="b5b3e-107">有幾個原生和舊版架構包含通用的架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="b5b3e-108">方法設定和方法認證中所使用的通用元素會抽象化成單一架構檔案，稱為「一般架構」。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="b5b3e-109">"Method configuration" 和 "connection properties" 這兩個詞彙可交換使用。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="b5b3e-110">同樣地，「方法認證」和「使用者屬性」等詞彙也會交替使用。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="b5b3e-111">EAPHost 架構</span><span class="sxs-lookup"><span data-stu-id="b5b3e-111">EAPHost Schema</span></span>



| <span data-ttu-id="b5b3e-112">結構描述</span><span class="sxs-lookup"><span data-stu-id="b5b3e-112">Schema</span></span>                                                                        | <span data-ttu-id="b5b3e-113">Description</span><span class="sxs-lookup"><span data-stu-id="b5b3e-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b5b3e-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="b5b3e-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="b5b3e-115">包含一般設定架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="b5b3e-116">baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="b5b3e-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="b5b3e-117">包含一般的認證架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="b5b3e-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="b5b3e-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="b5b3e-119">包含 **EapMethodType** 元素定義。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="b5b3e-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="b5b3e-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="b5b3e-121">包含 EAPHost 設定架構。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="b5b3e-122">eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="b5b3e-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="b5b3e-123">包含 EAPHost 認證架構。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="b5b3e-124">舊版架構</span><span class="sxs-lookup"><span data-stu-id="b5b3e-124">Legacy Schema</span></span>



| <span data-ttu-id="b5b3e-125">結構描述</span><span class="sxs-lookup"><span data-stu-id="b5b3e-125">Schema</span></span>                                                                            | <span data-ttu-id="b5b3e-126">Description</span><span class="sxs-lookup"><span data-stu-id="b5b3e-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5b3e-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="b5b3e-128">包含一般設定架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="b5b3e-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="b5b3e-130">包含一般的認證架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="b5b3e-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="b5b3e-132">包含一般設定架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="b5b3e-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="b5b3e-134">包含一般的認證架構元素。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="b5b3e-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="b5b3e-136">使用 EAP-TLS 來描述驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="b5b3e-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b5b3e-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="b5b3e-138">使用 EAP-TLS 來描述從 Windows 7 開始的驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="b5b3e-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="b5b3e-140">使用 EAP-TLS 來描述驗證認證和認證選項。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="b5b3e-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="b5b3e-142">可搭配 MS-CHAPv2 用來描述驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="b5b3e-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="b5b3e-144">搭配 MS-CHAPv2 使用，以描述驗證認證和認證選項。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="b5b3e-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="b5b3e-146">可搭配 PEAPv0 用來描述驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="b5b3e-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="b5b3e-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="b5b3e-148">與 PEAPv0 搭配使用，以描述從 Windows 7 開始的驗證設定資料。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="b5b3e-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b5b3e-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="b5b3e-150">與 PEAPv0 搭配使用，以描述驗證認證和認證選項。</span><span class="sxs-lookup"><span data-stu-id="b5b3e-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="b5b3e-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5b3e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b3e-152">查看 EAPHost 和舊版架構範例</span><span class="sxs-lookup"><span data-stu-id="b5b3e-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




