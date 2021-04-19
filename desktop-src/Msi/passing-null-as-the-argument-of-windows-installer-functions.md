---
description: 傳回使用者所提供之資料的 Windows Installer 函式–不應以 null 做為指標的值來呼叫記憶體位置。
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: 傳遞 null 給 Windows Installer 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979049"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="0f10f-103">傳遞 null 做為 Windows Installer 函數的引數</span><span class="sxs-lookup"><span data-stu-id="0f10f-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="0f10f-104">傳回使用者所提供之資料的 Windows Installer 函式–不應以 null 做為指標的值來呼叫記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="0f10f-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="0f10f-105">這些函式會傳回字串或傳回資料作為整數指標，但在傳遞 null 作為輸出引數的值時，會傳回不一致的值。</span><span class="sxs-lookup"><span data-stu-id="0f10f-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="0f10f-106">請勿傳遞 Null 作為下列任何函式的 output 引數值：</span><span class="sxs-lookup"><span data-stu-id="0f10f-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="0f10f-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="0f10f-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="0f10f-108">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="0f10f-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="0f10f-109">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="0f10f-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="0f10f-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="0f10f-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="0f10f-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="0f10f-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="0f10f-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="0f10f-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="0f10f-113">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="0f10f-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="0f10f-114">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="0f10f-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="0f10f-115">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="0f10f-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="0f10f-116">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="0f10f-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="0f10f-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="0f10f-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="0f10f-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="0f10f-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="0f10f-119">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="0f10f-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="0f10f-120">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="0f10f-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



