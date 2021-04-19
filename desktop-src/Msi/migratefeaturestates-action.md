---
description: 在升級期間，以及透過相關應用程式安裝新的應用程式時，會使用 MigrateFeatureStates 動作。
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: MigrateFeatureStates 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979961"
---
# <a name="migratefeaturestates-action"></a><span data-ttu-id="d9bed-103">MigrateFeatureStates 動作</span><span class="sxs-lookup"><span data-stu-id="d9bed-103">MigrateFeatureStates Action</span></span>

<span data-ttu-id="d9bed-104">在升級期間，以及透過相關應用程式安裝新的應用程式時，會使用 MigrateFeatureStates 動作。</span><span class="sxs-lookup"><span data-stu-id="d9bed-104">The MigrateFeatureStates action is used during upgrading and when installing a new application over a related application.</span></span> <span data-ttu-id="d9bed-105">MigrateFeatureStates 會讀取現有應用程式中的功能狀態，然後在擱置安裝中設定這些功能狀態。</span><span class="sxs-lookup"><span data-stu-id="d9bed-105">MigrateFeatureStates reads the feature states in the existing application and then sets these feature states in the pending installation.</span></span> <span data-ttu-id="d9bed-106">只有當新的功能樹狀結構並未大幅地從原始的變更時，此方法才有用。</span><span class="sxs-lookup"><span data-stu-id="d9bed-106">The method is only useful when the new feature tree has not greatly changed from the original.</span></span>

<span data-ttu-id="d9bed-107">只有在第一次安裝產品時，才會執行 MigrateFeatureStates 動作。</span><span class="sxs-lookup"><span data-stu-id="d9bed-107">The MigrateFeatureStates action only runs the first time the product is installed.</span></span> <span data-ttu-id="d9bed-108">MigrateFeatureStates 動作不會在維護模式或卸載期間執行。</span><span class="sxs-lookup"><span data-stu-id="d9bed-108">The MigrateFeatureStates action does not run during maintenance mode or uninstallation.</span></span>

<span data-ttu-id="d9bed-109">MigrateFeatureStates 動作會依序執行每個 [升級資料表](upgrade-table.md) 的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的所有產品進行比較。</span><span class="sxs-lookup"><span data-stu-id="d9bed-109">MigrateFeatureStates action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to all products installed on the system.</span></span> <span data-ttu-id="d9bed-110">如果 MigrateFeatureStates 動作偵測到通訊，而且在升級資料表的 [屬性] 資料行中設定 msidbUpgradeAttributesMigrateFeatures 位旗標，則安裝程式會查詢產品的現有功能狀態，並針對新應用程式中的相同功能設定這些狀態。</span><span class="sxs-lookup"><span data-stu-id="d9bed-110">If MigrateFeatureStates action detects a correspondence, and if the msidbUpgradeAttributesMigrateFeatures bit flag is set in the Attributes column of the Upgrade table, the installer queries the existing feature states for the product and sets these states for the same features in the new application.</span></span> <span data-ttu-id="d9bed-111">只有未設定 [**預先**](preselected.md) 選取的屬性時，動作才會遷移功能狀態。</span><span class="sxs-lookup"><span data-stu-id="d9bed-111">The action only migrates the feature states if the [**Preselected**](preselected.md) property is not set.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d9bed-112">順序限制</span><span class="sxs-lookup"><span data-stu-id="d9bed-112">Sequence Restrictions</span></span>

<span data-ttu-id="d9bed-113">MigrateFeatureStates 動作應該緊接在 [CostFinalize 動作](costfinalize-action.md)之後。</span><span class="sxs-lookup"><span data-stu-id="d9bed-113">The MigrateFeatureStates action should come immediately after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="d9bed-114">MigrateFeatureStates 必須在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排序。</span><span class="sxs-lookup"><span data-stu-id="d9bed-114">MigrateFeatureStates must be sequenced in both the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="d9bed-115">如果動作已在 InstallUISequence 中執行，則安裝程式會防止 MigrateFeatureStates 在 InstallExecuteSequence 中執行。</span><span class="sxs-lookup"><span data-stu-id="d9bed-115">The installer prevents MigrateFeatureStates from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d9bed-116">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="d9bed-116">ActionData Messages</span></span>

<span data-ttu-id="d9bed-117">MigrateFeatureSettings 會傳送每項產品的動作資料訊息。</span><span class="sxs-lookup"><span data-stu-id="d9bed-117">MigrateFeatureSettings sends an action data message for each product.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9bed-118">備註</span><span class="sxs-lookup"><span data-stu-id="d9bed-118">Remarks</span></span>

<span data-ttu-id="d9bed-119">如果有多個已安裝的產品共用功能，則該功能的安裝狀態可能會在產品之間不同。</span><span class="sxs-lookup"><span data-stu-id="d9bed-119">If more than one installed product shares a feature, the installation state for that feature may differ between products.</span></span> <span data-ttu-id="d9bed-120">MigrateFeatureState 動作在遷移功能安裝狀態時，會使用下列優先順序：執行本機、從來源執行、公告和卸載。</span><span class="sxs-lookup"><span data-stu-id="d9bed-120">MigrateFeatureState action uses the following order of precedence when migrating feature installation states: run local, run from source, advertised, and uninstalled.</span></span> <span data-ttu-id="d9bed-121">例如，已安裝的產品 A 可能具有 INSTALLSTATE 本機的功能 Y \_ ，且安裝的產品 B 可能會有功能 y，因為 INSTALLSTATE 不 \_ 存在。</span><span class="sxs-lookup"><span data-stu-id="d9bed-121">For example, installed product A may have feature Y as INSTALLSTATE\_LOCAL and installed product B may have feature Y as INSTALLSTATE\_ABSENT.</span></span> <span data-ttu-id="d9bed-122">如果升級會安裝產品 C 並遷移功能 Y 的安裝狀態，MigrateFeatureState 會將 product C 中的功能 Y 安裝狀態設定為 INSTALLSTATE \_ LOCAL。</span><span class="sxs-lookup"><span data-stu-id="d9bed-122">If an upgrade installs product C and migrates the installation state of feature Y, MigrateFeatureState sets the installation state of feature Y in product C to INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="d9bed-123">如需有關如何使用 MigrateFeatureStates 動作進行產品升級的詳細資訊，請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="d9bed-123">For more information about how to use the MigrateFeatureStates action for product upgrades, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

 

 



