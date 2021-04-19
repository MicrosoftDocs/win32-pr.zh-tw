---
description: XPS 數位簽章 API 介面
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: XPS 數位簽章 API 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985329"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="0c977-103">XPS 數位簽章 API 介面</span><span class="sxs-lookup"><span data-stu-id="0c977-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="0c977-104">目錄</span><span class="sxs-lookup"><span data-stu-id="0c977-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0c977-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="0c977-105">In this section</span></span>



| <span data-ttu-id="0c977-106">介面</span><span class="sxs-lookup"><span data-stu-id="0c977-106">Interface</span></span>                                                                           | <span data-ttu-id="0c977-107">描述</span><span class="sxs-lookup"><span data-stu-id="0c977-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c977-108">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="0c977-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="0c977-109">代表單一數位簽章。</span><span class="sxs-lookup"><span data-stu-id="0c977-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="0c977-110">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="0c977-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="0c977-111">表示儲存在 SignatureDefinitions 元件中的簽章要求區塊。</span><span class="sxs-lookup"><span data-stu-id="0c977-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="0c977-112">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="0c977-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="0c977-113">[**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)介面的集合。</span><span class="sxs-lookup"><span data-stu-id="0c977-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="0c977-114">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="0c977-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="0c977-115">[**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)介面指標的集合。</span><span class="sxs-lookup"><span data-stu-id="0c977-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="0c977-116">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="0c977-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="0c977-117">管理 XPS 檔的數位簽章和數位簽章要求。</span><span class="sxs-lookup"><span data-stu-id="0c977-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="0c977-118">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="0c977-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="0c977-119">存取簽章要求的元件。</span><span class="sxs-lookup"><span data-stu-id="0c977-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="0c977-120">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="0c977-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="0c977-121">[**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)介面的集合。</span><span class="sxs-lookup"><span data-stu-id="0c977-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="0c977-122">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="0c977-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="0c977-123">提供新簽章使用之個別簽署選項的存取權。</span><span class="sxs-lookup"><span data-stu-id="0c977-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




