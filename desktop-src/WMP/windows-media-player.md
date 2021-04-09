---
title: Windows Media Player
description: Windows Media Player
ms.assetid: 5a7452c4-5778-439b-b3e3-4e6311bef276
keywords:
- Windows Media Player，關於
- SDK (軟體發展工具組) ，功能
- 軟體發展工具組 (SDK) ，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2187ae6c7ae1cd0cd0b38616ab36f934f69bee94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021215"
---
# <a name="windows-media-player"></a><span data-ttu-id="63661-106">Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="63661-106">Windows Media Player</span></span>

<span data-ttu-id="63661-107">Windows Media Player SDK 提供的功能會影響 Windows Mobile Windows Media Player 和 Windows Media Player 的行為。</span><span class="sxs-lookup"><span data-stu-id="63661-107">The Windows Media Player SDK provides features that affect the behavior of Windows Media Player and Windows Media Player for Windows Mobile.</span></span>

<span data-ttu-id="63661-108">下列各節詳細說明一般適用于 Windows Media Player 的 SDK 功能。</span><span class="sxs-lookup"><span data-stu-id="63661-108">The following sections detail SDK features that apply to Windows Media Player in general.</span></span>



| <span data-ttu-id="63661-109">區段</span><span class="sxs-lookup"><span data-stu-id="63661-109">Section</span></span>                                                                                                        | <span data-ttu-id="63661-110">描述</span><span class="sxs-lookup"><span data-stu-id="63661-110">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63661-111">登錄設定</span><span class="sxs-lookup"><span data-stu-id="63661-111">Registry Settings</span></span>](registry-settings.md)                                                                     | <span data-ttu-id="63661-112">詳細說明您可以在使用者的登錄中變更的值，讓 Windows Media Player 辨識自訂副檔名。</span><span class="sxs-lookup"><span data-stu-id="63661-112">Details values that you can change in the user's registry to enable Windows Media Player to recognize custom file name extensions.</span></span>                                    |
| [<span data-ttu-id="63661-113">命令列參數</span><span class="sxs-lookup"><span data-stu-id="63661-113">Command Line Parameters</span></span>](command-line-parameters.md)                                                         | <span data-ttu-id="63661-114">詳細說明命令列參數的集合，這些參數會指定在啟動時 Windows Media Player 的行為。</span><span class="sxs-lookup"><span data-stu-id="63661-114">Details the set of command line parameters that specify how Windows Media Player behaves when it starts.</span></span>                                                              |
| [<span data-ttu-id="63661-115">音訊輸出</span><span class="sxs-lookup"><span data-stu-id="63661-115">Audio Outputs</span></span>](audio-outputs.md)                                                                             | <span data-ttu-id="63661-116">描述 Windows Media Player 和 Windows Media Player ActiveX 控制項如何選擇預設音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="63661-116">Describes how Windows Media Player and the Windows Media Player ActiveX control choose default audio output devices.</span></span>                                                  |
| [<span data-ttu-id="63661-117">轉散發 Windows Media Player 軟體</span><span class="sxs-lookup"><span data-stu-id="63661-117">Redistributing Windows Media Player Software</span></span>](redistributing-windows-media-player-software.md)               | <span data-ttu-id="63661-118">提供轉散發 Windows Media Player 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="63661-118">Provides information about redistributing Windows Media Player.</span></span>                                                                                                       |
| [<span data-ttu-id="63661-119">發佈 Windows Media Player 的編解碼器</span><span class="sxs-lookup"><span data-stu-id="63661-119">Publishing Codecs for Windows Media Player</span></span>](publishing-codecs-for-windows-media-player.md)                   | <span data-ttu-id="63661-120">不再支援在 WMPlugins 網站上發佈編解碼器。</span><span class="sxs-lookup"><span data-stu-id="63661-120">Publishing your codec on the WMPlugins website is no longer supported.</span></span>                                                                                                |
| [<span data-ttu-id="63661-121">調整授權取得對話方塊的大小</span><span class="sxs-lookup"><span data-stu-id="63661-121">Resizing the License Acquisition Dialog Box</span></span>](resizing-the-license-acquisition-dialog-box.md)                 | <span data-ttu-id="63661-122">說明如何修改 Windows Media 檔案屬性，以指定 Windows Media Player 10 或更新版本的授權取得對話方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="63661-122">Describes how to modify a Windows Media file attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span>                     |
| [<span data-ttu-id="63661-123">加速中繼資料傳輸的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="63661-123">Device Extensions for Accelerated Metadata Transfer</span></span>](device-extensions-for-accelerated-metadata-transfer.md) | <span data-ttu-id="63661-124">描述 Windows Media Player 如何從可攜式裝置抓取有關同步處理會話之間特定內容專案變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="63661-124">Describes how Windows Media Player retrieves information from portable devices about changes that occur to particular content items between synchronization sessions.</span></span> |
| [<span data-ttu-id="63661-125">用於報告取得內容的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="63661-125">Device Extensions for Reporting Acquired Content</span></span>](device-extensions-for-reporting-acquired-content.md)       | <span data-ttu-id="63661-126">描述 Windows Media Player 可如何在同步處理會話之間取得可攜式裝置所取得的新內容清單。</span><span class="sxs-lookup"><span data-stu-id="63661-126">Describes how Windows Media Player can retrieve a list of new content acquired by a portable device between synchronization sessions.</span></span>                                 |
| [<span data-ttu-id="63661-127">播放清單物件喜好設定的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="63661-127">Device Extensions for Playlist Object Preferences</span></span>](device-extensions-for-playlist-object-preferences.md)     | <span data-ttu-id="63661-128">描述可攜式裝置如何指定 Windows Media Player 必須在自動同步處理期間複製到裝置的播放清單物件類型。</span><span class="sxs-lookup"><span data-stu-id="63661-128">Describes how a portable device can specify which playlist object types Windows Media Player must copy to the device during automatic synchronization.</span></span>                |
| [<span data-ttu-id="63661-129">裝置 i/o 控制碼</span><span class="sxs-lookup"><span data-stu-id="63661-129">Device I/O Control Codes</span></span>](device-i-o-control-codes.md)                                                       | <span data-ttu-id="63661-130">列出 Windows Media Player 10 或更新版本用來透過 Windows Media 裝置管理員 SDK 與可攜式裝置通訊的裝置 i/o 控制碼。</span><span class="sxs-lookup"><span data-stu-id="63661-130">Lists device I/O control codes used by Windows Media Player 10 or later to communicate with portable devices through the Windows Media Device Manager SDK.</span></span>            |
| [<span data-ttu-id="63661-131">裝置的自訂映射支援</span><span class="sxs-lookup"><span data-stu-id="63661-131">Custom Image Support for Devices</span></span>](custom-image-support-for-devices.md)                                       | <span data-ttu-id="63661-132">描述可攜裝置製造商建立的兩個影像檔案，以自訂 Windows Media Player 10 或更新版本中的品牌。</span><span class="sxs-lookup"><span data-stu-id="63661-132">Describes two image files that portable device manufacturers can create to customize branding in Windows Media Player 10 or later.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="63661-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="63661-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63661-134">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="63661-134">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




