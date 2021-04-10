---
title: 網路診斷架構
description: 網路診斷架構 (NDF) 提供一種方法讓元件和應用程式開發人員簡化使用者的網路疑難排解。
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021155"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="3937e-103">網路診斷架構</span><span class="sxs-lookup"><span data-stu-id="3937e-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="3937e-104">目的</span><span class="sxs-lookup"><span data-stu-id="3937e-104">Purpose</span></span>

<span data-ttu-id="3937e-105">網路診斷架構 (NDF) 提供一種方法讓元件和應用程式開發人員簡化使用者的網路疑難排解。</span><span class="sxs-lookup"><span data-stu-id="3937e-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="3937e-106">使用者可以使用單一疑難排解工具來嘗試診斷和修復網路問題。</span><span class="sxs-lookup"><span data-stu-id="3937e-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="3937e-107">Microsoft 提供 NDF 協助程式類別，其中一些可延伸，讓開發人員可以建立稱為協助程式類別延伸的疑難排解單位，以提供特定軟體或硬體元件的更詳細診斷。</span><span class="sxs-lookup"><span data-stu-id="3937e-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3937e-108">適用時</span><span class="sxs-lookup"><span data-stu-id="3937e-108">Where applicable</span></span>

<span data-ttu-id="3937e-109">所有依賴網路連線能力的廠商軟體都可以使用 NDF。</span><span class="sxs-lookup"><span data-stu-id="3937e-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3937e-110">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="3937e-110">Developer audience</span></span>

<span data-ttu-id="3937e-111">NDF API 是針對 C/c + + 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="3937e-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3937e-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="3937e-112">Run-time requirements</span></span>

<span data-ttu-id="3937e-113">NDF 適用于執行 Windows Vista、Windows Server 2008 或更新版本的電腦。</span><span class="sxs-lookup"><span data-stu-id="3937e-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3937e-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="3937e-114">In this section</span></span>



| <span data-ttu-id="3937e-115">主題</span><span class="sxs-lookup"><span data-stu-id="3937e-115">Topic</span></span>                                                                       | <span data-ttu-id="3937e-116">描述</span><span class="sxs-lookup"><span data-stu-id="3937e-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3937e-117">關於 NDF</span><span class="sxs-lookup"><span data-stu-id="3937e-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="3937e-118">提供 NDF 技術的一般摘要。</span><span class="sxs-lookup"><span data-stu-id="3937e-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="3937e-119">使用 NDF</span><span class="sxs-lookup"><span data-stu-id="3937e-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="3937e-120">提供使用 NDF 功能的相關資訊和範例，以及如何擴充此功能。</span><span class="sxs-lookup"><span data-stu-id="3937e-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3937e-121">NDF 參考</span><span class="sxs-lookup"><span data-stu-id="3937e-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="3937e-122">提供支援使用 NDF 的列舉、函式、介面和結構的相關資訊，以及 Microsoft 提供的可延伸 helper 類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3937e-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="3937e-123">Windows 7 中的網路追蹤</span><span class="sxs-lookup"><span data-stu-id="3937e-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="3937e-124">討論用於疑難排解的網路追蹤和工具。</span><span class="sxs-lookup"><span data-stu-id="3937e-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 





