---
description: 自訂應用程式（例如公司範本）所需的資源，可以透過包含應用程式安裝套件的轉換來與應用程式一起部署。
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: 使用轉換來新增資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986943"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="0166a-103">使用轉換來新增資源</span><span class="sxs-lookup"><span data-stu-id="0166a-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="0166a-104">自訂應用程式（例如公司範本）所需的資源，可以透過包含應用程式安裝套件的轉換來與應用程式一起部署。</span><span class="sxs-lookup"><span data-stu-id="0166a-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="0166a-105">使用轉換來部署資源（例如檔案、登錄機碼或快速鍵）時，應遵循下列規則。</span><span class="sxs-lookup"><span data-stu-id="0166a-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="0166a-106">轉換應該將一或多個新元件新增至安裝資料庫，以包含其他資源。</span><span class="sxs-lookup"><span data-stu-id="0166a-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="0166a-107">轉換不應將資源新增至已存在於安裝中的元件。</span><span class="sxs-lookup"><span data-stu-id="0166a-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="0166a-108">轉換應該將一或多個新功能新增至安裝資料庫，以包含這些新元件。</span><span class="sxs-lookup"><span data-stu-id="0166a-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="0166a-109">這些新功能不應該是任何現有功能的父系，但可能會同時引進新的父項和子功能。</span><span class="sxs-lookup"><span data-stu-id="0166a-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="0166a-110">新功能的名稱應該是在此產品的所有其他轉換中都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0166a-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="0166a-111">這兩項轉換都不應該在 [功能資料表](feature-table.md) 的 feature 資料行中所列的相同名稱的產品中新增功能，並包含不同的元件或資源。</span><span class="sxs-lookup"><span data-stu-id="0166a-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



