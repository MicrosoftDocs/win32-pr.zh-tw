---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: PrintCapabilities 公用關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975606"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="8201d-104">PrintCapabilities 公用關鍵字</span><span class="sxs-lookup"><span data-stu-id="8201d-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="8201d-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="8201d-105">This topic is not current.</span></span> <span data-ttu-id="8201d-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="8201d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8201d-107">下一節會指定可用於 PrintCapabilities 檔的使用者可設定元素和參數定義。</span><span class="sxs-lookup"><span data-stu-id="8201d-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="8201d-108">使用者可設定的專案使用方式</span><span class="sxs-lookup"><span data-stu-id="8201d-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="8201d-109">使用者可設定的元素代表可能出現在 PrintCapabilities 檔或 PrintTicket 中的列印架構公用關鍵字。</span><span class="sxs-lookup"><span data-stu-id="8201d-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="8201d-110">它們的目的是要代表特定裝置所支援的可設定裝置屬性，或由應用程式或使用者傳達列印設定意圖。</span><span class="sxs-lookup"><span data-stu-id="8201d-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="8201d-111">使用者可設定的專案可以參考參數參考元素。</span><span class="sxs-lookup"><span data-stu-id="8201d-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="8201d-112">如需詳細資訊，請參閱 [參數參考元素](parameter-reference-elements.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="8201d-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="8201d-113">參數定義使用方式</span><span class="sxs-lookup"><span data-stu-id="8201d-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="8201d-114">參數定義在列印功能檔中採用 ParameterDef 元素類型的形式。</span><span class="sxs-lookup"><span data-stu-id="8201d-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="8201d-115">ParameterDef 元素類型會使用 ParameterInit 專案類型在 PrintTicket 中初始化。</span><span class="sxs-lookup"><span data-stu-id="8201d-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="8201d-116">參數的值將使用 ParameterInit 元素來指定。</span><span class="sxs-lookup"><span data-stu-id="8201d-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="8201d-117">使用者可設定的關鍵字可以使用 ParameterRef 元素類型來參考參數定義。</span><span class="sxs-lookup"><span data-stu-id="8201d-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="8201d-118">如需詳細資訊，請參閱 [參數結構](parameter-constructs.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="8201d-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8201d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8201d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8201d-120">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="8201d-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



