---
description: 應用程式必須呼叫幾個函數才能要求功能。
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: 要求功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026984"
---
# <a name="requesting-a-feature"></a><span data-ttu-id="abb04-103">要求功能</span><span class="sxs-lookup"><span data-stu-id="abb04-103">Requesting a Feature</span></span>

<span data-ttu-id="abb04-104">應用程式必須呼叫幾個函數才能要求功能。</span><span class="sxs-lookup"><span data-stu-id="abb04-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="abb04-105">在要求功能之前，應用程式必須確定已安裝此功能。</span><span class="sxs-lookup"><span data-stu-id="abb04-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="abb04-106">如果應用程式在應用程式存取功能之前呼叫 [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) ，應用程式可以使用傳回的資訊來維持使用計量。</span><span class="sxs-lookup"><span data-stu-id="abb04-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="abb04-107">**要求功能**</span><span class="sxs-lookup"><span data-stu-id="abb04-107">**To request a feature**</span></span>

1.  <span data-ttu-id="abb04-108">如果您想要判斷功能的可用性，而不遞增使用量計數，請呼叫 [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) 或 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) 函數。</span><span class="sxs-lookup"><span data-stu-id="abb04-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="abb04-109">藉由呼叫 [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) 函式，指出應用程式要使用功能的意圖。</span><span class="sxs-lookup"><span data-stu-id="abb04-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="abb04-110">藉由呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函數來判斷檔案位置。</span><span class="sxs-lookup"><span data-stu-id="abb04-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="abb04-111">藉由呼叫 [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) 函數來設定此功能。</span><span class="sxs-lookup"><span data-stu-id="abb04-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="abb04-112">藉由呼叫 [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) 函數來取得應用程式可使用的使用計量。</span><span class="sxs-lookup"><span data-stu-id="abb04-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="abb04-113">下圖說明功能要求模型。</span><span class="sxs-lookup"><span data-stu-id="abb04-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="abb04-114">功能要求模型。</span><span class="sxs-lookup"><span data-stu-id="abb04-114">feature request model.</span></span> ](images/over2.png)

 

 



