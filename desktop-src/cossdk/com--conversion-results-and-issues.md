---
description: 無論您選擇手動將 MTS 套件轉換為 COM + 應用程式，或讓 Microsoft Windows 安裝程式自動為您進行，您應該留意轉換的結果以及問題。
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: COM + 轉換結果和問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386012"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="0c09b-103">COM + 轉換結果和問題</span><span class="sxs-lookup"><span data-stu-id="0c09b-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="0c09b-104">無論您選擇手動將 MTS 套件轉換為 COM + 應用程式，或讓 Microsoft Windows 安裝程式自動為您進行，您應該留意轉換的結果以及問題。</span><span class="sxs-lookup"><span data-stu-id="0c09b-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="0c09b-105">轉換的內容</span><span class="sxs-lookup"><span data-stu-id="0c09b-105">What Is Converted</span></span>

<span data-ttu-id="0c09b-106">在轉換期間，MTSTOCOM 公用程式會轉換角色、角色指派、介面、方法、使用者、電腦清單，以及大部分的電腦設定。</span><span class="sxs-lookup"><span data-stu-id="0c09b-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="0c09b-107">MTSTOCOM 公用程式也會轉換 MTS 套件的身分識別和密碼。</span><span class="sxs-lookup"><span data-stu-id="0c09b-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="0c09b-108">在 MTS 中無法使用的新 COM + 屬性會自動設定為所有已轉換之 MTS 元件的下列預設值。</span><span class="sxs-lookup"><span data-stu-id="0c09b-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="0c09b-109">您可以使用 [元件服務] 系統管理工具或 COM + 系統管理介面變更這些預設值。</span><span class="sxs-lookup"><span data-stu-id="0c09b-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="0c09b-110">啟用 JIT 啟用。</span><span class="sxs-lookup"><span data-stu-id="0c09b-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="0c09b-111">物件共用已停用。</span><span class="sxs-lookup"><span data-stu-id="0c09b-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="0c09b-112">與交易設定相同的同步處理。</span><span class="sxs-lookup"><span data-stu-id="0c09b-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="0c09b-113">轉換問題</span><span class="sxs-lookup"><span data-stu-id="0c09b-113">Conversion Issues</span></span>

<span data-ttu-id="0c09b-114">當您安裝 Windows 時，系統會自動安裝 COM +。</span><span class="sxs-lookup"><span data-stu-id="0c09b-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="0c09b-115">不可能卸載 COM +。</span><span class="sxs-lookup"><span data-stu-id="0c09b-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="0c09b-116">與現有 MTS 和 COM + 安裝的升級相關的問題包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="0c09b-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="0c09b-117">如果您目前使用的是 MTS 1.0，則會自動將 MTS 升級至 COM +。</span><span class="sxs-lookup"><span data-stu-id="0c09b-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="0c09b-118">不過，使用者定義的封裝將會遺失，因此您必須重新建立它們。</span><span class="sxs-lookup"><span data-stu-id="0c09b-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="0c09b-119">如果您目前使用的是 MTS 2.0，則會自動將 MTS 升級至 COM +。</span><span class="sxs-lookup"><span data-stu-id="0c09b-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="0c09b-120">所有使用者定義的封裝將會升級至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c09b-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="0c09b-121">所有元件的運作方式應該與在 MTS 2.0 下的元件相同。</span><span class="sxs-lookup"><span data-stu-id="0c09b-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="0c09b-122">如果您使用的是 MTS 1.0 和 MTS 2.0 並已安裝 SDK 選項，將會移除 SDK 檔案。</span><span class="sxs-lookup"><span data-stu-id="0c09b-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="0c09b-123">您可以透過 Microsoft Windows SDK 安裝最新的 COM + SDK。</span><span class="sxs-lookup"><span data-stu-id="0c09b-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="0c09b-124">您無法從 COM + 電腦管理遠端 MTS 電腦。</span><span class="sxs-lookup"><span data-stu-id="0c09b-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c09b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c09b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c09b-126">從 MTS 自動轉換</span><span class="sxs-lookup"><span data-stu-id="0c09b-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="0c09b-127">從 MTS 手動轉換</span><span class="sxs-lookup"><span data-stu-id="0c09b-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="0c09b-128">MTS 管理程式庫</span><span class="sxs-lookup"><span data-stu-id="0c09b-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



