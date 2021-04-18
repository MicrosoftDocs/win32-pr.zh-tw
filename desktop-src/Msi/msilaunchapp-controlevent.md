---
description: 此控制項事件會執行指定的檔案。 如果檔案不存在，或事件失敗，Windows Installer 會將錯誤記錄在詳細資訊記錄檔中，而不會顯示包含錯誤訊息的對話方塊。
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983392"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="b2cd9-104">MsiLaunchApp ControlEvent</span><span class="sxs-lookup"><span data-stu-id="b2cd9-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="b2cd9-105">此控制項事件會執行指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-105">This control event runs a specified file.</span></span> <span data-ttu-id="b2cd9-106">如果檔案不存在，或事件失敗，Windows Installer 會將錯誤記錄在詳細資訊記錄檔中，而不會顯示包含錯誤訊息的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="b2cd9-107">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="b2cd9-108">從 Windows Installer 5.0 開始提供此 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="b2cd9-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="b2cd9-109">Published By</span></span>

<span data-ttu-id="b2cd9-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b2cd9-111">引數</span><span class="sxs-lookup"><span data-stu-id="b2cd9-111">Argument</span></span>

<span data-ttu-id="b2cd9-112">引數值的欄位會以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="b2cd9-113">第一個欄位包含指定要執行之檔案的字串值。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="b2cd9-114">使用 filekey 的字串值 \[ \#  \] 來識別檔案，並將 *filekey* 取代 [為檔案](file-table.md)資料表的 file 資料行中顯示的檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="b2cd9-115">引數的任何剩餘欄位都可以包含正在執行之檔案所使用的參數。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b2cd9-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="b2cd9-116">Action on Subscribers</span></span>

<span data-ttu-id="b2cd9-117">此 ControlEvent 不會在訂閱者上執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b2cd9-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="b2cd9-118">Typical Use</span></span>

<span data-ttu-id="b2cd9-119">讓使用者選擇在安裝結束時執行檔案。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="b2cd9-120">此事件可以在安裝的最後一個對話方塊上顯示的 [核取方塊](checkbox-control.md) 控制項設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="b2cd9-121">移除套件時不應顯示 CheckBox 控制項。</span><span class="sxs-lookup"><span data-stu-id="b2cd9-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



