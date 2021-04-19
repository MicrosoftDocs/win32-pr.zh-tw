---
title: 自訂圖示縮圖和即時預覽點陣圖
description: 示範如何自訂 iconic 縮圖和即時預覽點陣圖 (也稱為查看預覽) 。
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106993928"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="026f6-103">自訂圖示縮圖和即時預覽點陣圖</span><span class="sxs-lookup"><span data-stu-id="026f6-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="026f6-104">Description</span><span class="sxs-lookup"><span data-stu-id="026f6-104">Description</span></span>

<span data-ttu-id="026f6-105">您可以使用 Windows 7 桌面視窗管理員 (DWM) Api 中引進的函式和訊息，自訂 iconic 縮圖和 *即時預覽* (或 *查看預覽*) 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="026f6-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="026f6-106">具體而言，您會使用 [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) 函數和 [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) 訊息來自訂 iconic 縮圖。</span><span class="sxs-lookup"><span data-stu-id="026f6-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="026f6-107">您也可以使用 [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式和 [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) 訊息來設定 iconic live preview 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="026f6-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="026f6-108">如需使用 **DwmSetIconicThumbnail** 函數的範例應用程式，請參閱 [TabThumbnails 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails)。</span><span class="sxs-lookup"><span data-stu-id="026f6-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="026f6-109">下圖顯示轉換成自訂縮圖的預設縮圖。</span><span class="sxs-lookup"><span data-stu-id="026f6-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![使用自訂點陣圖的原始縮圖影像和修改後縮圖影像的圖例](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="026f6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="026f6-111">Requirements</span></span>

| <span data-ttu-id="026f6-112">需求</span><span class="sxs-lookup"><span data-stu-id="026f6-112">Requirement</span></span> | <span data-ttu-id="026f6-113">值</span><span class="sxs-lookup"><span data-stu-id="026f6-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="026f6-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="026f6-114">Minimum supported client</span></span> | <span data-ttu-id="026f6-115">Windows 7 或 Windows Vista Service Pack 2 (SP2) 和 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="026f6-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="026f6-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="026f6-116">Minimum supported server</span></span> | <span data-ttu-id="026f6-117">Windows Server 2008 R2 或 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="026f6-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="026f6-118">最小 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="026f6-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="026f6-119">適用于 Windows 7 的 Windows 軟體開發套件 (SDK) </span><span class="sxs-lookup"><span data-stu-id="026f6-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="026f6-120">建立 TabThumbnails 範例</span><span class="sxs-lookup"><span data-stu-id="026f6-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="026f6-121">**若要使用 Microsoft Visual Studio (慣用方法來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="026f6-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="026f6-122">開啟 Windows 檔案總管，然後流覽至 TabThumbnails .sln 檔案所在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="026f6-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="026f6-123">按兩下方案檔 ( .sln) 開啟 Microsoft Visual Studio 中的檔案。</span><span class="sxs-lookup"><span data-stu-id="026f6-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="026f6-124">在 [建置] 功能表上，按一下 [建置方案]。</span><span class="sxs-lookup"><span data-stu-id="026f6-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="026f6-125">應用程式是以預設的 \\ Debug 或 \\ Release 目錄來建立。</span><span class="sxs-lookup"><span data-stu-id="026f6-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="026f6-126">**若要使用命令提示字元建立範例**</span><span class="sxs-lookup"><span data-stu-id="026f6-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="026f6-127">開啟 [命令提示字元] 視窗，並流覽至範例目錄。</span><span class="sxs-lookup"><span data-stu-id="026f6-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="026f6-128">輸入 `msbuild TabThumbnails.sln`。</span><span class="sxs-lookup"><span data-stu-id="026f6-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="026f6-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="026f6-129">Related topics</span></span>

[<span data-ttu-id="026f6-130">桌面視窗管理員</span><span class="sxs-lookup"><span data-stu-id="026f6-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="026f6-131">Windows 程式開發</span><span class="sxs-lookup"><span data-stu-id="026f6-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
