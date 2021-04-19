---
description: 這是會話物件的 Mode 屬性。 這個屬性是一個值，代表目前安裝會話的指定模式旗標。 大部分的模式旗標在外部是唯讀的，但您也可以設定幾個指定的旗標。
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session. Mode 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001938"
---
# <a name="sessionmode-property"></a><span data-ttu-id="c623a-105">Session. Mode 屬性</span><span class="sxs-lookup"><span data-stu-id="c623a-105">Session.Mode property</span></span>

<span data-ttu-id="c623a-106">這是 [**會話**](session-object.md)物件的 **Mode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c623a-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="c623a-107">這個屬性是一個值，代表目前安裝會話的指定模式旗標。</span><span class="sxs-lookup"><span data-stu-id="c623a-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="c623a-108">大部分的模式旗標在外部是唯讀的，但您也可以設定幾個指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="c623a-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="c623a-109">[**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)函式會傳回布林值 TRUE 或 FALSE，指出傳遞至函式的特定屬性目前是否已設定 (TRUE) 或未設定 (FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="c623a-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="c623a-110">請注意，從延遲的自訂動作呼叫 **mode** 屬性時，不會提供 *旗* 標的所有執行模式值。</span><span class="sxs-lookup"><span data-stu-id="c623a-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="c623a-111">如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="c623a-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="c623a-112">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c623a-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c623a-113">語法</span><span class="sxs-lookup"><span data-stu-id="c623a-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="c623a-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="c623a-114">Property value</span></span>

<span data-ttu-id="c623a-115">旗標的必要整數值。</span><span class="sxs-lookup"><span data-stu-id="c623a-115">Required integer value for the flag.</span></span> <span data-ttu-id="c623a-116">必須是下列其中之一：</span><span class="sxs-lookup"><span data-stu-id="c623a-116">Must be one of the following:</span></span>



| <span data-ttu-id="c623a-117">旗標名稱</span><span class="sxs-lookup"><span data-stu-id="c623a-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="c623a-118">意義</span><span class="sxs-lookup"><span data-stu-id="c623a-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="c623a-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="c623a-120">系統管理模式安裝，否則為產品安裝。</span><span class="sxs-lookup"><span data-stu-id="c623a-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="c623a-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="c623a-122">安裝的公告模式。</span><span class="sxs-lookup"><span data-stu-id="c623a-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="c623a-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="c623a-124">已載入維護模式資料庫。</span><span class="sxs-lookup"><span data-stu-id="c623a-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="c623a-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="c623a-126">已啟用復原。</span><span class="sxs-lookup"><span data-stu-id="c623a-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="c623a-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="c623a-128">記錄檔正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c623a-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="c623a-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="c623a-130">執行或幕後處理作業。</span><span class="sxs-lookup"><span data-stu-id="c623a-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="c623a-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="c623a-132"> (可設定的) 需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="c623a-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="c623a-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="c623a-134">需要重新開機才能繼續安裝 (可設定的) 。</span><span class="sxs-lookup"><span data-stu-id="c623a-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="c623a-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="c623a-136">使用媒體資料表從封包和檔案安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="c623a-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="c623a-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="c623a-138">來源檔案只使用簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c623a-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="c623a-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="c623a-140">目標檔案只會使用簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c623a-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="c623a-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="c623a-142">作業系統是 Windows 98/95。</span><span class="sxs-lookup"><span data-stu-id="c623a-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="c623a-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="c623a-144">作業系統支援產品的廣告。</span><span class="sxs-lookup"><span data-stu-id="c623a-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="c623a-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="c623a-146">從安裝腳本執行呼叫的延後 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="c623a-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="c623a-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="c623a-148">從復原執行腳本呼叫的延後 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="c623a-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="c623a-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="c623a-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="c623a-150">從認可執行腳本呼叫的延後 [自訂動作](custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="c623a-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c623a-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="c623a-151">Requirements</span></span>



| <span data-ttu-id="c623a-152">需求</span><span class="sxs-lookup"><span data-stu-id="c623a-152">Requirement</span></span> | <span data-ttu-id="c623a-153">值</span><span class="sxs-lookup"><span data-stu-id="c623a-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c623a-154">版本</span><span class="sxs-lookup"><span data-stu-id="c623a-154">Version</span></span><br/> | <span data-ttu-id="c623a-155">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c623a-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c623a-156">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c623a-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c623a-157">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c623a-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




