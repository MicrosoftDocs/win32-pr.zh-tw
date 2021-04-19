---
description: 由於 Windows Installer 會保留關係資料庫中安裝的所有資訊，因此可以藉由將轉換作業套用至封裝，針對特定使用者群組自訂應用程式或產品的安裝。
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: 自訂
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981420"
---
# <a name="customization"></a><span data-ttu-id="d57d0-103">自訂</span><span class="sxs-lookup"><span data-stu-id="d57d0-103">Customization</span></span>

<span data-ttu-id="d57d0-104">由於 Windows Installer 會保留關係資料庫中安裝的所有資訊，因此可以藉由將轉換作業套用至封裝，針對特定使用者群組自訂應用程式或產品的安裝。</span><span class="sxs-lookup"><span data-stu-id="d57d0-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="d57d0-105">轉換可以用來封裝不同工作組所需之基底套件的各種自訂。</span><span class="sxs-lookup"><span data-stu-id="d57d0-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="d57d0-106">如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="d57d0-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="d57d0-107">在安裝期間，可以即時套用多個基底套件的轉換。</span><span class="sxs-lookup"><span data-stu-id="d57d0-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="d57d0-108">這提供了一種機制，可有效率地將自訂安裝指派給不同的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="d57d0-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="d57d0-109">例如，這在支援部門的公司需要不同的特定產品安裝時，才會很有用。</span><span class="sxs-lookup"><span data-stu-id="d57d0-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="d57d0-110">此產品可供組織中的所有人使用，方法是將基本套件的 [系統管理安裝](administrative-installation.md) 到單一系統管理安裝點。</span><span class="sxs-lookup"><span data-stu-id="d57d0-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="d57d0-111">然後每個工作群組都可以透過在安裝產品時的即時轉換，自動接收適當的自訂。</span><span class="sxs-lookup"><span data-stu-id="d57d0-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



