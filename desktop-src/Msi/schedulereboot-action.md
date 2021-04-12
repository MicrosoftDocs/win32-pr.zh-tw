---
description: 將 ScheduleReboot 動作插入動作順序，以提示使用者在安裝結束時重新開機系統。 使用 ForceReboot 動作，在安裝期間提示重新開機。
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: ScheduleReboot 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849330"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="6d20e-104">ScheduleReboot 動作</span><span class="sxs-lookup"><span data-stu-id="6d20e-104">ScheduleReboot Action</span></span>

<span data-ttu-id="6d20e-105">將 ScheduleReboot 動作插入動作順序，以提示使用者在安裝結束時重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="6d20e-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="6d20e-106">使用 [ForceReboot 動作](forcereboot-action.md) ，在安裝期間提示重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="6d20e-107">如果安裝具有使用者介面，安裝程式會在安裝結束時顯示訊息方塊和按鈕，詢問使用者是否想要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="6d20e-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="6d20e-108">使用者必須在完成安裝之前回應此提示。</span><span class="sxs-lookup"><span data-stu-id="6d20e-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="6d20e-109">如果安裝沒有使用者介面，系統會在結束時自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="6d20e-110">如果安裝程式判斷是否需要重新開機，它會自動提示使用者在安裝結束時重新開機，不論順序中是否有任何 ForceReboot 或 ScheduleReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="6d20e-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="6d20e-111">例如，如果安裝程式需要取代任何在安裝期間使用的檔案，安裝程式會自動提示重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="6d20e-112">您可以藉由設定 [ [**重新開機**](reboot.md) ] 屬性，隱藏某些提示以重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="6d20e-113">如果 Windows Installer 在[多套件安裝](multiple-package-installations.md)期間遇到[ForceReboot](forcereboot-action.md)或 ScheduleReboot 動作，安裝程式將會停止並復原安裝。</span><span class="sxs-lookup"><span data-stu-id="6d20e-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="6d20e-114">您可以安裝屬於多套件安裝的其他套件，而這些套件不包含 ForceReboot 或 ScheduleReboot 動作。</span><span class="sxs-lookup"><span data-stu-id="6d20e-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6d20e-115">順序限制</span><span class="sxs-lookup"><span data-stu-id="6d20e-115">Sequence Restrictions</span></span>

<span data-ttu-id="6d20e-116">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="6d20e-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6d20e-117">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="6d20e-117">ActionData Messages</span></span>

<span data-ttu-id="6d20e-118">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="6d20e-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d20e-119">備註</span><span class="sxs-lookup"><span data-stu-id="6d20e-119">Remarks</span></span>

<span data-ttu-id="6d20e-120">例如，您可以在安裝需要重新開機的驅動程式之後，使用此動作來強制安裝程式提示重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="6d20e-121">如果安裝程式嘗試取代使用中的檔案，即使尚未使用 ScheduleReboot，它也會自動提示使用者重新開機。</span><span class="sxs-lookup"><span data-stu-id="6d20e-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="6d20e-122">ScheduleReboot 動作通常會放在序列的結尾，但可插入序列中的任何時間點。</span><span class="sxs-lookup"><span data-stu-id="6d20e-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d20e-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d20e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d20e-124">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="6d20e-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



