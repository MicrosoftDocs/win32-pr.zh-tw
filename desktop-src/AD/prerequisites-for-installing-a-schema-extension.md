---
title: 安裝架構延伸模組的必要條件
description: 若要修改架構，請確定您擁有下列許可權，並注意下列資訊：您必須擁有足夠的許可權才能修改架構。
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314373"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="511af-103">安裝架構延伸模組的必要條件</span><span class="sxs-lookup"><span data-stu-id="511af-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="511af-104">若要修改架構，請確定您擁有下列許可權，並注意下列資訊：</span><span class="sxs-lookup"><span data-stu-id="511af-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="511af-105">您必須有足夠的許可權才能修改架構。</span><span class="sxs-lookup"><span data-stu-id="511af-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="511af-106">架構包含整個企業 Active Directory Domain Services 的所有資料定義。</span><span class="sxs-lookup"><span data-stu-id="511af-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="511af-107">若要更新架構，使用者必須是架構系統管理員群組的成員，或已被委派更新架構的許可權。</span><span class="sxs-lookup"><span data-stu-id="511af-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="511af-108">您只能在架構主機上進行架構變更。</span><span class="sxs-lookup"><span data-stu-id="511af-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="511af-109">如需詳細資訊，請參閱偵測 [架構主機](detecting-the-schema-master.md)。</span><span class="sxs-lookup"><span data-stu-id="511af-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="511af-110">架構主機必須是可寫入的;也就是說，必須移除登錄中的安全聯鎖。</span><span class="sxs-lookup"><span data-stu-id="511af-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="511af-111">如需詳細資訊，請參閱 [在架構主機上啟用架構變更](enabling-schema-changes-at-the-schema-master.md)。</span><span class="sxs-lookup"><span data-stu-id="511af-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="511af-112">如需如何檢查架構主機是否可以修改的詳細資訊，以及如何變更其設定，請參閱說明及支援知識庫中的「XADM：無法更新架構擁有者的架構」 [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) 。</span><span class="sxs-lookup"><span data-stu-id="511af-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




