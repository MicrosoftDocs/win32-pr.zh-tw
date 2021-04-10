---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable。
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7b86a726af95e7ec9fb764d5e752057a24b3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187692"
---
# <a name="ceipenable"></a><span data-ttu-id="b66aa-103">CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="b66aa-103">CEIPEnable</span></span>

<span data-ttu-id="b66aa-104">**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**</span><span class="sxs-lookup"><span data-stu-id="b66aa-104">**HKLM\\Software\\Microsoft\\SQMClient\\Windows\\CEIPEnable**</span></span>



| <span data-ttu-id="b66aa-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b66aa-105">Data type</span></span>  | <span data-ttu-id="b66aa-106">範圍</span><span class="sxs-lookup"><span data-stu-id="b66aa-106">Range</span></span>                     | <span data-ttu-id="b66aa-107">預設值</span><span class="sxs-lookup"><span data-stu-id="b66aa-107">Default value</span></span> |
|------------|---------------------------|---------------|
| <span data-ttu-id="b66aa-108">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="b66aa-108">REG\_DWORD</span></span> | <span data-ttu-id="b66aa-109">0 (停用) 或 1 (啟用) </span><span class="sxs-lookup"><span data-stu-id="b66aa-109">0 (disable) or 1 (enable)</span></span> | <span data-ttu-id="b66aa-110">0</span><span class="sxs-lookup"><span data-stu-id="b66aa-110">0</span></span>             |



 

## <a name="description"></a><span data-ttu-id="b66aa-111">Description</span><span class="sxs-lookup"><span data-stu-id="b66aa-111">Description</span></span>

<span data-ttu-id="b66aa-112">啟用 Windows 客戶經驗改進計畫。</span><span class="sxs-lookup"><span data-stu-id="b66aa-112">Enables the Windows Customer Experience Improvement program.</span></span>

## <a name="change-method"></a><span data-ttu-id="b66aa-113">變更方法</span><span class="sxs-lookup"><span data-stu-id="b66aa-113">Change Method</span></span>

<span data-ttu-id="b66aa-114">若要變更這個專案的值，請在 [主控台中，選取 [ **系統和維護**]，然後選取 [ **問題報告與解決方案**]。</span><span class="sxs-lookup"><span data-stu-id="b66aa-114">To change the value of this entry, in Control Panel, select **System and Maintenance**, followed by **Problem Reports and Solutions**.</span></span> <span data-ttu-id="b66aa-115">按一下 [另請參閱] 區段中的 [ **客戶經驗改進設定** ]。</span><span class="sxs-lookup"><span data-stu-id="b66aa-115">Click **Customer Experience Improvement Settings** from the See Also section.</span></span>

## <a name="activation-method"></a><span data-ttu-id="b66aa-116">啟用方法</span><span class="sxs-lookup"><span data-stu-id="b66aa-116">Activation Method</span></span>

<span data-ttu-id="b66aa-117">對此專案所做的變更會立即生效。</span><span class="sxs-lookup"><span data-stu-id="b66aa-117">Changes made to this entry are effective immediately.</span></span> <span data-ttu-id="b66aa-118">啟用此登錄機碼會讓整個電腦啟用 Windows 客戶經驗改進計畫。</span><span class="sxs-lookup"><span data-stu-id="b66aa-118">Enabling this registry key causes the Windows Customer Experience Improvement Program to be enabled for the entire computer.</span></span> <span data-ttu-id="b66aa-119">停用此登錄機碼會導致整個電腦的 Windows 客戶經驗改進計畫停用。</span><span class="sxs-lookup"><span data-stu-id="b66aa-119">Disabling this registry key causes the Windows Customer Experience Improvement Program to be disabled for the entire computer.</span></span>

<span data-ttu-id="b66aa-120">在支援群組原則的系統上，群組原則設定會取代此專案。</span><span class="sxs-lookup"><span data-stu-id="b66aa-120">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="b66aa-121">當 Windows 客戶經驗改進計畫 CEIP 啟用群組原則] 設定啟用時，系統會忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="b66aa-121">While the Windows Customer Experience Improvement Program CEIP Enable Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="b66aa-122">此原則設定的設定會儲存在 [ **HKLM \\ Software policy \\ \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**] 底下的 [**原則**] 區段中。</span><span class="sxs-lookup"><span data-stu-id="b66aa-122">The configuration of this policy setting is stored in the **Policies** section under **HKLM\\Software\\Policies\\Microsoft\\SQMClient\\Windows\\CEIPEnable**.</span></span>

 

 



