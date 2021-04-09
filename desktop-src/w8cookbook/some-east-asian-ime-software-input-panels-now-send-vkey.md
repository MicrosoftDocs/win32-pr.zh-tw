---
title: 某些東亞 IME 軟體輸入面板現在會傳送 vKey
description: 某些東亞 IME 軟體輸入面板現在會傳送 vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840896"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a><span data-ttu-id="d9955-103">某些東亞 IME 軟體輸入面板現在會傳送 vKey</span><span class="sxs-lookup"><span data-stu-id="d9955-103">Some East Asian IME software input panels now send vKey</span></span>

## <a name="platforms"></a><span data-ttu-id="d9955-104">平台</span><span class="sxs-lookup"><span data-stu-id="d9955-104">Platforms</span></span>

<dl> <span data-ttu-id="d9955-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="d9955-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="d9955-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d9955-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="d9955-107">Description</span><span class="sxs-lookup"><span data-stu-id="d9955-107">Description</span></span>

<span data-ttu-id="d9955-108">在 Windows 8 中，如果選取其中一個東亞 Ime，則按下軟體輸入面板鍵不會傳送 vKeys。</span><span class="sxs-lookup"><span data-stu-id="d9955-108">In Windows 8, if one of the East Asian IMEs is selected, pressing a software input panel key did not send vKeys.</span></span>

<span data-ttu-id="d9955-109">在 Windows 8.1 中，會針對下列設定傳送 vKeys：</span><span class="sxs-lookup"><span data-stu-id="d9955-109">In Windows 8.1, vKeys are sent for the following configurations:</span></span>



| <span data-ttu-id="d9955-110">語言</span><span class="sxs-lookup"><span data-stu-id="d9955-110">Language</span></span>            | <span data-ttu-id="d9955-111">IME</span><span class="sxs-lookup"><span data-stu-id="d9955-111">IME</span></span>                                 | <span data-ttu-id="d9955-112">Windows 市集</span><span class="sxs-lookup"><span data-stu-id="d9955-112">Windows Store</span></span> | <span data-ttu-id="d9955-113">桌面</span><span class="sxs-lookup"><span data-stu-id="d9955-113">Desktop</span></span> |
|---------------------|-------------------------------------|---------------|---------|
| <span data-ttu-id="d9955-114">簡體中文</span><span class="sxs-lookup"><span data-stu-id="d9955-114">Simplified Chinese</span></span>  | <span data-ttu-id="d9955-115">Microsoft 拼音，Microsoft Wubi</span><span class="sxs-lookup"><span data-stu-id="d9955-115">Microsoft Pinyin, Microsoft Wubi</span></span>    | <span data-ttu-id="d9955-116">是</span><span class="sxs-lookup"><span data-stu-id="d9955-116">Yes</span></span>           | <span data-ttu-id="d9955-117">是</span><span class="sxs-lookup"><span data-stu-id="d9955-117">Yes</span></span>     |
| <span data-ttu-id="d9955-118">繁體中文</span><span class="sxs-lookup"><span data-stu-id="d9955-118">Traditional Chinese</span></span> | <span data-ttu-id="d9955-119">Microsoft Changlie，Microsoft 快速</span><span class="sxs-lookup"><span data-stu-id="d9955-119">Microsoft Changlie, Microsoft Quick</span></span> | <span data-ttu-id="d9955-120">是</span><span class="sxs-lookup"><span data-stu-id="d9955-120">Yes</span></span>           | <span data-ttu-id="d9955-121">是</span><span class="sxs-lookup"><span data-stu-id="d9955-121">Yes</span></span>     |
| <span data-ttu-id="d9955-122">繁體中文</span><span class="sxs-lookup"><span data-stu-id="d9955-122">Traditional Chinese</span></span> | <span data-ttu-id="d9955-123">Microsoft 注音</span><span class="sxs-lookup"><span data-stu-id="d9955-123">Microsoft Bopomofo</span></span>                  | <span data-ttu-id="d9955-124">否</span><span class="sxs-lookup"><span data-stu-id="d9955-124">No</span></span>            | <span data-ttu-id="d9955-125">否</span><span class="sxs-lookup"><span data-stu-id="d9955-125">No</span></span>      |
| <span data-ttu-id="d9955-126">韓文</span><span class="sxs-lookup"><span data-stu-id="d9955-126">Korean</span></span>              | <span data-ttu-id="d9955-127">[Microsoft IME]</span><span class="sxs-lookup"><span data-stu-id="d9955-127">Microsoft IME</span></span>                       | <span data-ttu-id="d9955-128">是</span><span class="sxs-lookup"><span data-stu-id="d9955-128">Yes</span></span>           | <span data-ttu-id="d9955-129">否</span><span class="sxs-lookup"><span data-stu-id="d9955-129">No</span></span>      |
| <span data-ttu-id="d9955-130">日文</span><span class="sxs-lookup"><span data-stu-id="d9955-130">Japanese</span></span>            | <span data-ttu-id="d9955-131">[Microsoft IME]</span><span class="sxs-lookup"><span data-stu-id="d9955-131">Microsoft IME</span></span>                       | <span data-ttu-id="d9955-132">否</span><span class="sxs-lookup"><span data-stu-id="d9955-132">No</span></span>            | <span data-ttu-id="d9955-133">否</span><span class="sxs-lookup"><span data-stu-id="d9955-133">No</span></span>      |



 

## <a name="manifestations"></a><span data-ttu-id="d9955-134">表現</span><span class="sxs-lookup"><span data-stu-id="d9955-134">Manifestations</span></span>

<span data-ttu-id="d9955-135">如果使用者選擇不傳送 vKeys 的輸入法，vKey 觸發的函式將無法運作。</span><span class="sxs-lookup"><span data-stu-id="d9955-135">If the user chooses an IME that does not send vKeys, vKey-triggered functions do not work.</span></span>

## <a name="solution"></a><span data-ttu-id="d9955-136">解決方法</span><span class="sxs-lookup"><span data-stu-id="d9955-136">Solution</span></span>

<span data-ttu-id="d9955-137">未使用上述其中一個 IME 設定的應用程式，必須設計成讓使用者可以完成所需的工作，而不需要使用需要 vKeys 的函式。</span><span class="sxs-lookup"><span data-stu-id="d9955-137">Applications that do not use one of the above IME configurations must be designed so that users can complete the desired task without using functions that require vKeys.</span></span>

<span data-ttu-id="d9955-138">如果使用者選擇執行傳送 vKeys 的輸入法，但應用程式是在不預期的情況下設計的，則必須變更應用程式，以辨識正在執行的 Windows 版本，並據以回應。</span><span class="sxs-lookup"><span data-stu-id="d9955-138">If the user chooses an IME that does send vKeys, but the application was designed without that expectation, the application must be changed to recognize which version of Windows is running and respond accordingly.</span></span>

 

 




