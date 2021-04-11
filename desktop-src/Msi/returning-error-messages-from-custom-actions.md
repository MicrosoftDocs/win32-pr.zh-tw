---
description: 本節說明如何藉由呼叫動態連結程式庫或腳本，從實際執行一部分安裝的自訂動作傳送訊息。
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: 從自訂動作傳回錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480a9e7891680aadc9d8eb4eedba2bad0d2e3dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114553"
---
# <a name="returning-error-messages-from-custom-actions"></a><span data-ttu-id="24bc8-103">從自訂動作傳回錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="24bc8-103">Returning Error Messages from Custom Actions</span></span>

<span data-ttu-id="24bc8-104">本節說明如何藉由呼叫動態連結程式庫或腳本，從實際執行一部分安裝的自訂動作傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="24bc8-104">This section describes how to send messages from custom actions that actually perform a part of the installation by calling a dynamic link library or script.</span></span> <span data-ttu-id="24bc8-105">請注意， [自訂動作類型 19](custom-action-type-19.md) 只會傳送指定的錯誤訊息、傳回失敗，然後結束安裝。</span><span class="sxs-lookup"><span data-stu-id="24bc8-105">Note that [Custom Action Type 19](custom-action-type-19.md) only sends a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="24bc8-106">自訂動作類型19不會執行安裝的任何部分。</span><span class="sxs-lookup"><span data-stu-id="24bc8-106">Custom Action Type 19 does not perform any part of the installation.</span></span>

<span data-ttu-id="24bc8-107">若要從使用 [動態連結程式庫](dynamic-link-libraries.md) (DLL) 的自訂動作傳送錯誤訊息，請使用自訂動作呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)。</span><span class="sxs-lookup"><span data-stu-id="24bc8-107">To send an error message from a custom action that uses a [dynamic-link library](dynamic-link-libraries.md) (DLL), have the custom action call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="24bc8-108">請注意， [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 啟動的自訂動作可以使用 [**Message**](session-message.md) 方法傳送訊息，但無法使用 **MsiProcessMessage** 傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="24bc8-108">Note that custom actions launched by a [DoAction ControlEvent](doaction-controlevent.md) can send messages with the [**Message**](session-message.md) method but cannot send a message with **MsiProcessMessage**.</span></span> <span data-ttu-id="24bc8-109">在 Windows Server 2003 之前的系統上，由 Dataadapter.doaction ControlEvent 啟動的自訂動作無法使用 **MsiProcessMessage** 或 **Message** 方法傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="24bc8-109">On systems earlier than Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message** method.</span></span> <span data-ttu-id="24bc8-110">如需詳細資訊，請參閱 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="24bc8-110">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="24bc8-111">**使用 DLL 在自訂動作內顯示錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="24bc8-111">**To display an error message from within a custom action using a DLL**</span></span>

1.  <span data-ttu-id="24bc8-112">自訂動作應該會呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，並傳入 *hInstall*、 *eMessageType* 和 *hRecord* 參數。</span><span class="sxs-lookup"><span data-stu-id="24bc8-112">The custom action should call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and pass in the parameters *hInstall*, *eMessageType*, and *hRecord*.</span></span> <span data-ttu-id="24bc8-113">[從自訂動作或 MsiOpenProduct 或 MsiOpenPackage 存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)中所述，可將安裝的控制碼（[自訂動作類型 19](custom-action-type-19.md)）提供給[](/windows/desktop/api/Msi/nf-msi-msiopenproducta)自訂[](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)動作。</span><span class="sxs-lookup"><span data-stu-id="24bc8-113">The handle to the installation, [Custom Action Type 19](custom-action-type-19.md), may be provided to the custom action as described in [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md) or from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea).</span></span>
2.  <span data-ttu-id="24bc8-114">參數 *eMessageType* 應指定其中一種訊息類型，如 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)中所列。</span><span class="sxs-lookup"><span data-stu-id="24bc8-114">The parameter *eMessageType* should specify one of the message types as listed in [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span>
3.  <span data-ttu-id="24bc8-115">[**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數的 *hRecord* 參數會根據訊息類型而定。</span><span class="sxs-lookup"><span data-stu-id="24bc8-115">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type.</span></span> <span data-ttu-id="24bc8-116">請參閱 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="24bc8-116">See [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span> <span data-ttu-id="24bc8-117">如果訊息包含格式化的資料，請使用 [[格式化](formatted.md)] 中所述的格式，將訊息輸入[錯誤](error-table.md)資料表。</span><span class="sxs-lookup"><span data-stu-id="24bc8-117">If the message contains formatted data, enter the message into the [Error](error-table.md) table using the formatting described in [Formatted](formatted.md).</span></span>

<span data-ttu-id="24bc8-118">若要從使用 [腳本](scripts.md)的自訂動作傳送錯誤訊息，自訂動作可能會呼叫 [**會話**](session-object.md)物件的 [**訊息**](session-message.md)方法。</span><span class="sxs-lookup"><span data-stu-id="24bc8-118">To send an error message from a custom action that uses [Scripts](scripts.md), the custom action may call the [**Message**](session-message.md) method of the [**Session**](session-object.md) object.</span></span>

<span data-ttu-id="24bc8-119">**使用腳本在自訂動作中顯示錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="24bc8-119">**To display an error message from within a custom action using script**</span></span>

1.  <span data-ttu-id="24bc8-120">自訂動作應呼叫 [**會話**](session-object.md)物件的 [**訊息**](session-message.md)方法，並傳入參數 *種類* 和 *記錄*。</span><span class="sxs-lookup"><span data-stu-id="24bc8-120">The custom action should call the [**Message**](session-message.md) method of the [**Session**](session-object.md) object and pass in the parameters *kind* and *record*.</span></span>
2.  <span data-ttu-id="24bc8-121">參數 *種類* 應該指定 [**訊息**](session-message.md) 方法中所列的其中一種訊息類型。</span><span class="sxs-lookup"><span data-stu-id="24bc8-121">The parameter *kind* should specify one of the message types listed in the [**Message**](session-message.md) method.</span></span>
3.  <span data-ttu-id="24bc8-122">[**Message**](session-message.md)方法的 *record* 參數會根據訊息類型而定。</span><span class="sxs-lookup"><span data-stu-id="24bc8-122">The *record* parameter of the [**Message**](session-message.md) method depends upon the message type.</span></span> <span data-ttu-id="24bc8-123">如果訊息包含格式化的資料，請使用 [[格式化](formatted.md)] 中所述的格式，將訊息輸入[錯誤](error-table.md)資料表。</span><span class="sxs-lookup"><span data-stu-id="24bc8-123">If the message contains formatted data, enter the message into the [Error](error-table.md) table using the formatting described in [Formatted](formatted.md).</span></span>

<span data-ttu-id="24bc8-124">使用 [可執行檔](executable-files.md) 的自訂動作無法藉由呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 或 [**message**](session-message.md) 方法來傳送訊息，因為它們無法取得安裝的控制碼。</span><span class="sxs-lookup"><span data-stu-id="24bc8-124">Custom actions using [Executable Files](executable-files.md) cannot send a message by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) or the [**Message**](session-message.md) method because they cannot get a handle to the installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24bc8-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="24bc8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24bc8-126">自訂動作傳回值</span><span class="sxs-lookup"><span data-stu-id="24bc8-126">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



