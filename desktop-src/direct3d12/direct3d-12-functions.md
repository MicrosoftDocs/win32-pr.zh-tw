---
title: " (Direct3D 12 圖形) 的核心功能"
description: 下列函數是在 d3d12 中宣告。
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "106993721"
---
# <a name="core-functions"></a><span data-ttu-id="4ca94-103">核心功能</span><span class="sxs-lookup"><span data-stu-id="4ca94-103">Core functions</span></span>

<span data-ttu-id="4ca94-104">下列函數是在 d3d12 中宣告。</span><span class="sxs-lookup"><span data-stu-id="4ca94-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ca94-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4ca94-105">In this section</span></span>

| <span data-ttu-id="4ca94-106">主題</span><span class="sxs-lookup"><span data-stu-id="4ca94-106">Topic</span></span> | <span data-ttu-id="4ca94-107">描述</span><span class="sxs-lookup"><span data-stu-id="4ca94-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="4ca94-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="4ca94-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="4ca94-109">建立代表顯示配接器的裝置。</span><span class="sxs-lookup"><span data-stu-id="4ca94-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="4ca94-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="4ca94-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="4ca94-111">還原序列化根簽章，讓您可以判斷 ([**D3D12 根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)) 的版面配置定義。</span><span class="sxs-lookup"><span data-stu-id="4ca94-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="4ca94-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="4ca94-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="4ca94-113">產生可透過 [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)傳回還原序列化之資料結構的介面。</span><span class="sxs-lookup"><span data-stu-id="4ca94-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="4ca94-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="4ca94-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="4ca94-115">啟用實驗性功能的清單。</span><span class="sxs-lookup"><span data-stu-id="4ca94-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="4ca94-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="4ca94-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="4ca94-117">取得 debug 介面。</span><span class="sxs-lookup"><span data-stu-id="4ca94-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="4ca94-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4ca94-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="4ca94-119">序列化可傳遞至 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)的根簽章版本1.0。</span><span class="sxs-lookup"><span data-stu-id="4ca94-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="4ca94-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4ca94-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="4ca94-121">序列化任何可以傳遞給 [**ID3D12Device：： CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)之版本的根簽章。</span><span class="sxs-lookup"><span data-stu-id="4ca94-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="4ca94-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ca94-122">Related topics</span></span>

* [<span data-ttu-id="4ca94-123">核心參考</span><span class="sxs-lookup"><span data-stu-id="4ca94-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="4ca94-124">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="4ca94-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






