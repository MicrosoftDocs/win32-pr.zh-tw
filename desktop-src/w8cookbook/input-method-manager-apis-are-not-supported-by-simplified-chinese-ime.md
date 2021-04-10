---
title: 簡體中文 IME 不支援輸入方法管理員 Api
description: 簡體中文 IME 不支援輸入方法管理員 Api
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092862"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="40b34-103">簡體中文 IME 不支援輸入方法管理員 Api</span><span class="sxs-lookup"><span data-stu-id="40b34-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="40b34-104">平台</span><span class="sxs-lookup"><span data-stu-id="40b34-104">Platforms</span></span>

<dl> <span data-ttu-id="40b34-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="40b34-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="40b34-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="40b34-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="40b34-107">Description</span><span class="sxs-lookup"><span data-stu-id="40b34-107">Description</span></span>

<span data-ttu-id="40b34-108">Windows 8.1 中的簡體中文 Ime 不支援下列輸入方法管理員 Api：</span><span class="sxs-lookup"><span data-stu-id="40b34-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="40b34-109">IFECommon 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-109">IFECommon interface</span></span>
-   <span data-ttu-id="40b34-110">IFEDictionary 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="40b34-111">IFELanguage 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-111">IFELanguage interface</span></span>
-   <span data-ttu-id="40b34-112">IImePad 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-112">IImePad interface</span></span>
-   <span data-ttu-id="40b34-113">IImePadApplet 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="40b34-114">IImeSpecifyApplets 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="40b34-115">表現</span><span class="sxs-lookup"><span data-stu-id="40b34-115">Manifestations</span></span>

<span data-ttu-id="40b34-116">使用這些 Api 的函式不適用於簡體中文 IME。</span><span class="sxs-lookup"><span data-stu-id="40b34-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="40b34-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="40b34-117">Solution</span></span>

<span data-ttu-id="40b34-118">應用程式必須經過設計，使用者才能完成所需的工作，而不需使用指定的 API。</span><span class="sxs-lookup"><span data-stu-id="40b34-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="40b34-119">資源</span><span class="sxs-lookup"><span data-stu-id="40b34-119">Resources</span></span>

-   [<span data-ttu-id="40b34-120">輸入方法管理員介面</span><span class="sxs-lookup"><span data-stu-id="40b34-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="40b34-121">IFECommon</span><span class="sxs-lookup"><span data-stu-id="40b34-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="40b34-122">IFECommon 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="40b34-123">IFEDictionary 介面</span><span class="sxs-lookup"><span data-stu-id="40b34-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="40b34-124">IFELanguage</span><span class="sxs-lookup"><span data-stu-id="40b34-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="40b34-125">IImePad</span><span class="sxs-lookup"><span data-stu-id="40b34-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="40b34-126">IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="40b34-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="40b34-127">IimePlugInDictDictionaryList</span><span class="sxs-lookup"><span data-stu-id="40b34-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="40b34-128">IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="40b34-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 