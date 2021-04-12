---
description: HKCU \\ 主控台 \\ Desktop。
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385974"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="385bd-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="385bd-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="385bd-104">**HKCU \\ 主控台 \\ Desktop**</span><span class="sxs-lookup"><span data-stu-id="385bd-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="385bd-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="385bd-105">Data type</span></span> | <span data-ttu-id="385bd-106">範圍</span><span class="sxs-lookup"><span data-stu-id="385bd-106">Range</span></span>       | <span data-ttu-id="385bd-107">預設值</span><span class="sxs-lookup"><span data-stu-id="385bd-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="385bd-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="385bd-108">REG\_SZ</span></span>   | <span data-ttu-id="385bd-109">*檔案名稱*</span><span class="sxs-lookup"><span data-stu-id="385bd-109">*File name*</span></span> | <span data-ttu-id="385bd-110">(無)</span><span class="sxs-lookup"><span data-stu-id="385bd-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="385bd-111">Description</span><span class="sxs-lookup"><span data-stu-id="385bd-111">Description</span></span>

<span data-ttu-id="385bd-112">指定螢幕保護裝置可執行檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="385bd-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="385bd-113">變更方法</span><span class="sxs-lookup"><span data-stu-id="385bd-113">Change Method</span></span>

<span data-ttu-id="385bd-114">若要變更這個專案的值，請在主控台按兩下 [ **顯示**] 中，按一下 [ **螢幕保護裝置** ] 索引標籤，然後從 [ **螢幕保護裝置** ] 清單中選取螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="385bd-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="385bd-115">您也可以使用應用程式開發介面來變更此專案， (API) 函式 **InstallScreenSaver**（由 Desk.cpl 匯出）。</span><span class="sxs-lookup"><span data-stu-id="385bd-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="385bd-116">您可以使用命令列 **rundll32.exe desk.cpl InstallScreenSaver** 檔來存取此函式，其中 *file* 是螢幕保護裝置可 *執行檔的* 名稱。</span><span class="sxs-lookup"><span data-stu-id="385bd-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="385bd-117">啟用方法</span><span class="sxs-lookup"><span data-stu-id="385bd-117">Activation Method</span></span>

<span data-ttu-id="385bd-118">當系統下次啟動畫面保護時，對此專案所做的變更就會變得有效。</span><span class="sxs-lookup"><span data-stu-id="385bd-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="385bd-119">當螢幕保護裝置正在執行時對此專案所做的變更，不會影響執行中的螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="385bd-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="385bd-120">備註</span><span class="sxs-lookup"><span data-stu-id="385bd-120">Notes</span></span>

-   <span data-ttu-id="385bd-121">當您在主控台中使用 [ **顯示** ] 來選取螢幕保護裝置時，Windows 作業系統會將此專案新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="385bd-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="385bd-122">如果您從 [螢幕保護裝置程式] 清單中選擇 **([無])** 來停用所有螢幕保護裝置，則作業系統會從登錄中刪除這個專案，並呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式，其 *UiAction* 等於 SPI \_ SETSCREENSAVEACTIVE， *uiParam* 等於 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="385bd-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="385bd-123">在支援群組原則的系統上，群組原則設定會取代此專案。</span><span class="sxs-lookup"><span data-stu-id="385bd-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="385bd-124">啟用 **螢幕保護裝置可執行檔名稱** 群組原則設定時，系統會忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="385bd-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="385bd-125">此原則設定的設定會儲存在 **SCRNSAVE.EXE** 專案中，該專案位於 **原則** 子機碼中。</span><span class="sxs-lookup"><span data-stu-id="385bd-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
