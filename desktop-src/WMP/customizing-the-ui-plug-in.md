---
title: 自訂 UI 外掛程式
description: 自訂 UI 外掛程式
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Windows Media Player 外掛程式，自訂
- 外掛程式，自訂
- 使用者介面外掛程式，自訂
- UI 外掛程式，自訂
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021857"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="1208c-107">自訂 UI 外掛程式</span><span class="sxs-lookup"><span data-stu-id="1208c-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="1208c-108">至此，您的專案已經準備好進行自訂。</span><span class="sxs-lookup"><span data-stu-id="1208c-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="1208c-109">您可以修改 wizard 產生的 **IWMPPluginUI** 介面，您可以將使用者介面加入至 **CPluginWindow** 類別，也可以在 **CPropertyDialog** 類別中執行屬性頁。</span><span class="sxs-lookup"><span data-stu-id="1208c-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="1208c-110">如果您的外掛程式設定為接聽 Windows Media Player 事件，則嚮導會產生所有必要的事件處理常式（您也可以修改或建立）的預設或空白的執行。</span><span class="sxs-lookup"><span data-stu-id="1208c-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="1208c-111">外掛程式的類型及其支援的功能，會以儲存在 Windows 登錄中的值來表示。</span><span class="sxs-lookup"><span data-stu-id="1208c-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="1208c-112">Wizard 會產生副檔名為 .rgs 的檔案，其中包含用來註冊外掛程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="1208c-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="1208c-113">此檔案中的「功能」值是布林值或 wmpplug 中所定義外掛程式類型常數和外掛程式旗標的十進位對等專案。</span><span class="sxs-lookup"><span data-stu-id="1208c-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="1208c-114">雖然此值取決於您在嚮導中選取的選項，但是如果您想要建立具有多個預設值的外掛程式，或是可以傳送媒體專案或播放清單的外掛程式，就必須修改此值。</span><span class="sxs-lookup"><span data-stu-id="1208c-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="1208c-115">當您修改和擴充外掛程式程式碼時，可以建立並註冊您的 DLL，以便在 Windows Media Player 中測試您的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="1208c-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1208c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1208c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1208c-117">**建立 UI 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="1208c-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




