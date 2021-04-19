---
description: 會話物件會控制安裝程式。
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: '會話物件 (Windows Installer) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997743"
---
# <a name="session-object-windows-installer"></a><span data-ttu-id="7d876-103">會話物件 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="7d876-103">Session object (Windows Installer)</span></span>

<span data-ttu-id="7d876-104">**會話** 物件會控制安裝程式。</span><span class="sxs-lookup"><span data-stu-id="7d876-104">The **Session** object controls the installation process.</span></span> <span data-ttu-id="7d876-105">它會開啟安裝程式資料庫，其中包含安裝資料表和資料。</span><span class="sxs-lookup"><span data-stu-id="7d876-105">It opens the Installer database, which contains the installation tables and data.</span></span> <span data-ttu-id="7d876-106">這個物件與一組標準動作函式相關聯，每個都對一或多個資料表的資料執行特定作業。</span><span class="sxs-lookup"><span data-stu-id="7d876-106">This object is associated with a standard set of action functions, each performing particular operations on data from one or more tables.</span></span> <span data-ttu-id="7d876-107">您可以針對特定產品安裝新增額外的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="7d876-107">Additional custom actions may be added for particular product installations.</span></span> <span data-ttu-id="7d876-108">基本引擎函數是從指定順序資料表中提取順序記錄、評估任何指定的條件運算式，並執行指定動作的 sequencer。</span><span class="sxs-lookup"><span data-stu-id="7d876-108">The basic engine function is a sequencer that fetches sequential records from a designated sequence table, evaluates any specified condition expression, and executes the designated action.</span></span> <span data-ttu-id="7d876-109">引擎無法辨識的動作會延後至 UI 處理常式物件以進行處理，通常是對話方塊序列。</span><span class="sxs-lookup"><span data-stu-id="7d876-109">Actions not recognized by the engine are deferred to the UI handler object for processing, usually dialog box sequences.</span></span>

<span data-ttu-id="7d876-110">請注意，單一進程只能開啟一個 **會話** 物件。</span><span class="sxs-lookup"><span data-stu-id="7d876-110">Note that only one **Session** object can be opened by a single process.</span></span>

## <a name="members"></a><span data-ttu-id="7d876-111">成員</span><span class="sxs-lookup"><span data-stu-id="7d876-111">Members</span></span>

<span data-ttu-id="7d876-112">**Session** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7d876-112">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="7d876-113">方法</span><span class="sxs-lookup"><span data-stu-id="7d876-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="7d876-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7d876-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7d876-115">方法</span><span class="sxs-lookup"><span data-stu-id="7d876-115">Methods</span></span>

<span data-ttu-id="7d876-116">**Session** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7d876-116">The **Session** object has these methods.</span></span>



| <span data-ttu-id="7d876-117">方法</span><span class="sxs-lookup"><span data-stu-id="7d876-117">Method</span></span>                                                 | <span data-ttu-id="7d876-118">描述</span><span class="sxs-lookup"><span data-stu-id="7d876-118">Description</span></span>                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d876-119">**Dataadapter.doaction**</span><span class="sxs-lookup"><span data-stu-id="7d876-119">**DoAction**</span></span>](session-doaction.md)                   | <span data-ttu-id="7d876-120">執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="7d876-120">Executes the specified action.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="7d876-121">**EvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="7d876-121">**EvaluateCondition**</span></span>](session-evaluatecondition.md) | <span data-ttu-id="7d876-122">評估包含符號和值的邏輯運算式，並傳回列舉 msiEvaluateConditionErrorEnum 的整數。</span><span class="sxs-lookup"><span data-stu-id="7d876-122">Evaluates a logical expression containing symbols and values and returns an integer of the enumeration msiEvaluateConditionErrorEnum.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="7d876-123">**FeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="7d876-123">**FeatureInfo**</span></span>](session-featureinfo.md)             | <span data-ttu-id="7d876-124">傳回 [**FeatureInfo**](featureinfo-object.md) 物件，其中包含指定功能的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="7d876-124">Returns a [**FeatureInfo**](featureinfo-object.md) object containing descriptive information for the specified feature.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="7d876-125">**FormatRecord**</span><span class="sxs-lookup"><span data-stu-id="7d876-125">**FormatRecord**</span></span>](session-formatrecord.md)           | <span data-ttu-id="7d876-126">從範本和記錄資料傳回格式化的字串。</span><span class="sxs-lookup"><span data-stu-id="7d876-126">Returns a formatted string from template and record data.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="7d876-127">**消息**</span><span class="sxs-lookup"><span data-stu-id="7d876-127">**Message**</span></span>](session-message.md)                     | <span data-ttu-id="7d876-128">執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="7d876-128">Performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="7d876-129">**序列**</span><span class="sxs-lookup"><span data-stu-id="7d876-129">**Sequence**</span></span>](session-sequence.md)                   | <span data-ttu-id="7d876-130">在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。</span><span class="sxs-lookup"><span data-stu-id="7d876-130">Opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="7d876-131">針對每個提取的資料列，如果任何提供的條件運算式未評估為 False，則會呼叫 [**dataadapter.doaction**](session-doaction.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d876-131">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span><br/> |
| [<span data-ttu-id="7d876-132">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="7d876-132">**SetInstallLevel**</span></span>](session-setinstalllevel.md)     | <span data-ttu-id="7d876-133">將目前安裝的安裝層級設定為指定的值，並重新計算所有功能的 [選取] 和 [已安裝] 狀態。</span><span class="sxs-lookup"><span data-stu-id="7d876-133">Sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features.</span></span><br/>                                                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="7d876-134">屬性</span><span class="sxs-lookup"><span data-stu-id="7d876-134">Properties</span></span>

<span data-ttu-id="7d876-135">**Session** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7d876-135">The **Session** object has these properties.</span></span>



| <span data-ttu-id="7d876-136">屬性</span><span class="sxs-lookup"><span data-stu-id="7d876-136">Property</span></span>                                                                  | <span data-ttu-id="7d876-137">存取類型</span><span class="sxs-lookup"><span data-stu-id="7d876-137">Access type</span></span>           | <span data-ttu-id="7d876-138">Description</span><span class="sxs-lookup"><span data-stu-id="7d876-138">Description</span></span>                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d876-139">**ComponentCosts**</span><span class="sxs-lookup"><span data-stu-id="7d876-139">**ComponentCosts**</span></span>](session-componentcosts.md)<br/>               |                       | <span data-ttu-id="7d876-140">傳回 [**RecordList**](recordlist-object.md) 物件，此物件會列舉安裝元件所需的每個磁片磁碟機的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="7d876-140">Returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span><br/>                                  |
| [<span data-ttu-id="7d876-141">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="7d876-141">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)<br/> |                       | <span data-ttu-id="7d876-142">傳回指定元件目前已安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d876-142">Returns the current installed state of the designated component.</span></span><br/>                                                                                                |
| [<span data-ttu-id="7d876-143">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="7d876-143">**ComponentRequestState**</span></span>](session-componentrequeststate.md)<br/> |                       | <span data-ttu-id="7d876-144">取得或要求元件資料表中資料列的動作狀態變更。</span><span class="sxs-lookup"><span data-stu-id="7d876-144">Obtains or requests a change in the Action state of a row in the Component table.</span></span><br/>                                                                               |
| [<span data-ttu-id="7d876-145">**資料庫**</span><span class="sxs-lookup"><span data-stu-id="7d876-145">**Database**</span></span>](session-database.md)<br/>                           |                       | <span data-ttu-id="7d876-146">傳回目前安裝會話的資料庫。</span><span class="sxs-lookup"><span data-stu-id="7d876-146">Returns the database for the current installation session.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="7d876-147">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="7d876-147">**FeatureCost**</span></span>](session-featurecost.md)<br/>                     |                       | <span data-ttu-id="7d876-148">傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) ) 的功能資料表的根目錄 (。</span><span class="sxs-lookup"><span data-stu-id="7d876-148">Returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span><br/> |
| [<span data-ttu-id="7d876-149">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="7d876-149">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)<br/>     |                       | <span data-ttu-id="7d876-150">傳回指定功能目前已安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d876-150">Returns the current installed state of the designated feature.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="7d876-151">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="7d876-151">**FeatureRequestState**</span></span>](session-featurerequeststate.md)<br/>     | <span data-ttu-id="7d876-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7d876-152">Read/write</span></span><br/> | <span data-ttu-id="7d876-153">取得或要求功能記錄和子記錄的選取狀態變更。</span><span class="sxs-lookup"><span data-stu-id="7d876-153">Obtains or requests a change in the Select state of a feature's record and subrecords.</span></span><br/>                                                                          |
| [<span data-ttu-id="7d876-154">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="7d876-154">**FeatureValidStates**</span></span>](session-featurevalidstates.md)<br/>       |                       | <span data-ttu-id="7d876-155">傳回代表位旗標的整數，每個相關位表示指定功能的有效安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="7d876-155">Returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span><br/>                             |
| [<span data-ttu-id="7d876-156">**安裝程式**</span><span class="sxs-lookup"><span data-stu-id="7d876-156">**Installer**</span></span>](session-installer.md)<br/>                         |                       | <span data-ttu-id="7d876-157">傳回使用中的安裝程式物件。</span><span class="sxs-lookup"><span data-stu-id="7d876-157">Returns the active installer object.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="7d876-158">**Language (Session 物件)**</span><span class="sxs-lookup"><span data-stu-id="7d876-158">**Language (Session Object)**</span></span>](session-language.md)<br/>          |                       | <span data-ttu-id="7d876-159">表示目前安裝會話所使用的數位語言識別項。</span><span class="sxs-lookup"><span data-stu-id="7d876-159">Represents the numeric language identifier used by the current installation session.</span></span><br/>                                                                            |
| [<span data-ttu-id="7d876-160">**模式**</span><span class="sxs-lookup"><span data-stu-id="7d876-160">**Mode**</span></span>](session-mode.md)<br/>                                   |                       | <span data-ttu-id="7d876-161">這個屬性是一個值，代表目前安裝會話的指定模式旗標。</span><span class="sxs-lookup"><span data-stu-id="7d876-161">This property is a value representing the designated mode flag for the current installation session.</span></span><br/>                                                            |
| [<span data-ttu-id="7d876-162">**ProductProperty**</span><span class="sxs-lookup"><span data-stu-id="7d876-162">**ProductProperty**</span></span>](session-productproperty.md)<br/>             |                       | <span data-ttu-id="7d876-163">表示命名安裝程式屬性的字串值。</span><span class="sxs-lookup"><span data-stu-id="7d876-163">Represents the string value of a named installer property.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="7d876-164">**屬性 (會話物件)**</span><span class="sxs-lookup"><span data-stu-id="7d876-164">**Property (Session Object)**</span></span>](session-session.md)<br/>           | <span data-ttu-id="7d876-165">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7d876-165">Read/write</span></span><br/> | <span data-ttu-id="7d876-166">從產品資料庫抓取產品屬性。</span><span class="sxs-lookup"><span data-stu-id="7d876-166">Retrieves product properties from the product database.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="7d876-167">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="7d876-167">**SourcePath**</span></span>](session-sourcepath.md)<br/>                       |                       | <span data-ttu-id="7d876-168">提供來源媒體或伺服器映射上指定之資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7d876-168">Provides the full path to the designated folder on the source media or server image.</span></span><br/>                                                                            |
| [<span data-ttu-id="7d876-169">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="7d876-169">**TargetPath**</span></span>](session-targetpath.md)<br/>                       | <span data-ttu-id="7d876-170">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7d876-170">Read/write</span></span><br/> | <span data-ttu-id="7d876-171">提供安裝目標磁片磁碟機上所指定資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7d876-171">Provides the full path to the designated folder on the installation target drive.</span></span><br/>                                                                               |
| [<span data-ttu-id="7d876-172">**VerifyDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="7d876-172">**VerifyDiskSpace**</span></span>](session-verifydiskspace.md)<br/>             |                       | <span data-ttu-id="7d876-173">如果有足夠的磁碟空間，則傳回 true，如果磁片已滿，則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="7d876-173">Returns true if enough disk space exists, and false if the disk is full.</span></span><br/>                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="7d876-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d876-174">Requirements</span></span>



| <span data-ttu-id="7d876-175">需求</span><span class="sxs-lookup"><span data-stu-id="7d876-175">Requirement</span></span> | <span data-ttu-id="7d876-176">值</span><span class="sxs-lookup"><span data-stu-id="7d876-176">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d876-177">版本</span><span class="sxs-lookup"><span data-stu-id="7d876-177">Version</span></span><br/> | <span data-ttu-id="7d876-178">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7d876-178">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7d876-179">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7d876-179">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7d876-180">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7d876-180">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7d876-181">DLL</span><span class="sxs-lookup"><span data-stu-id="7d876-181">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d876-182"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d876-182"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7d876-183">IID</span><span class="sxs-lookup"><span data-stu-id="7d876-183">IID</span></span><br/>     | <span data-ttu-id="7d876-184">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7d876-184">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="7d876-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d876-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d876-186">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="7d876-186">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




