---
description: 有幾個功能會變更產品元件和功能的安裝。 以下說明如何變更功能和元件。
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: 使用功能和元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983735"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="25857-104">使用功能和元件</span><span class="sxs-lookup"><span data-stu-id="25857-104">Working with Features and Components</span></span>

<span data-ttu-id="25857-105">有幾個功能會變更產品 [元件和功能](components-and-features.md)的安裝。</span><span class="sxs-lookup"><span data-stu-id="25857-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="25857-106">以下說明如何變更功能和元件。</span><span class="sxs-lookup"><span data-stu-id="25857-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="25857-107">**變更功能和元件的安裝**</span><span class="sxs-lookup"><span data-stu-id="25857-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="25857-108">藉由呼叫 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) 函數來設定元件或功能的安裝層級。</span><span class="sxs-lookup"><span data-stu-id="25857-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="25857-109">封裝中的每項功能都會被指派 [功能資料表](feature-table.md)中的安裝層級。</span><span class="sxs-lookup"><span data-stu-id="25857-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="25857-110">如果功能的安裝層級低於 [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)所設定的層級，則會選取此功能進行安裝。</span><span class="sxs-lookup"><span data-stu-id="25857-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="25857-111">呼叫 **MsiSetInstallLevel** 之後，您可以明確變更是否已安裝功能。</span><span class="sxs-lookup"><span data-stu-id="25857-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="25857-112">藉由呼叫 [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) 函式來判斷指定功能可使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="25857-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="25857-113">藉由呼叫 [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) 函式，取得指定功能及其子功能的磁碟空間需求。</span><span class="sxs-lookup"><span data-stu-id="25857-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="25857-114">藉由呼叫 [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) 函式或 [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) 函數來取得功能或元件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="25857-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="25857-115">使用 [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) 函數或 [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) 函數來變更功能或元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="25857-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



