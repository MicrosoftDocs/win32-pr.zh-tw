---
description: Windows 影像處理元件 (WIC) 提供 IWICColorCoNtext 介面和 IWICColorTransform 介面，以簡化色彩管理。
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: 色彩管理總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990437"
---
# <a name="color-management-overview"></a><span data-ttu-id="5748a-103">色彩管理總覽</span><span class="sxs-lookup"><span data-stu-id="5748a-103">Color Management Overview</span></span>

<span data-ttu-id="5748a-104">數位影像源自並以各種裝置為目標，每個裝置都有自己的範圍和動態範圍。</span><span class="sxs-lookup"><span data-stu-id="5748a-104">Digital images originate from and are targeted at a variety of devices, each of which has its own gamut and dynamic range.</span></span> <span data-ttu-id="5748a-105">如果您的攝影師是在兩個不同的攝影機上捕捉相同的場景，則即使在相同的輸出裝置上轉譯，結果影像中的色彩也不會完全相同，因為兩個來源裝置的色彩範圍功能不同。</span><span class="sxs-lookup"><span data-stu-id="5748a-105">If a photographer were to capture the same scene on two different cameras, the colors in the resulting images would not appear exactly the same, even when rendered on the same output device because the color gamut capabilities of the two source devices were different.</span></span> <span data-ttu-id="5748a-106">同樣地，在兩個不同目標裝置上轉譯的相同影像將會以不同的方式呈現，因為目標裝置具有不同的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="5748a-106">Likewise, the same image rendered on two different target devices will appear differently because the target devices have different color profiles.</span></span> <span data-ttu-id="5748a-107">為了確保跨裝置進行一致的色彩複製，必須建立從來源裝置的色彩設定檔到目標裝置的色彩設定檔的對應。</span><span class="sxs-lookup"><span data-stu-id="5748a-107">To ensure consistent color reproduction across devices, it's necessary to create a mapping from the color profile of the source device to the color profile of the target device.</span></span> <span data-ttu-id="5748a-108">色彩管理旨在產生接近且一致的視覺效果比對，而且是專業映射中的重要功能。</span><span class="sxs-lookup"><span data-stu-id="5748a-108">Color management seeks to produce a close and consistent visual match and is a critical feature in professional imaging.</span></span>

<span data-ttu-id="5748a-109">能夠一致地重現掃描器、監視器、印表機和應用程式的色彩，聽起來像是簡單的目標，但是在作業系統中沒有色彩管理系統，就很難達成。</span><span class="sxs-lookup"><span data-stu-id="5748a-109">Being able to consistently reproduce color across scanners, monitors, printers, and applications sounds like a simple goal, but without a color management system in the operating system, it's difficult to achieve.</span></span> <span data-ttu-id="5748a-110">如果每個應用程式都需要產生自己的色彩設定檔，則幾乎無法在整個發佈程式中達到一致的色彩交換，包括掃描、編輯和撰寫、校對和散發。</span><span class="sxs-lookup"><span data-stu-id="5748a-110">If each application is required to generate its own color profiles, it's almost impossible to achieve consistent color interchange throughout the publishing process, which includes scanning, editing and composition, proofing, and distribution.</span></span>

<span data-ttu-id="5748a-111">Windows 影像處理元件 (WIC) 提供 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)介面和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)介面，以簡化色彩管理。您可以使用 [**IWICFactory：： CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer)取得 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)物件。</span><span class="sxs-lookup"><span data-stu-id="5748a-111">Windows Imaging Component (WIC) simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.You can get an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) object using the [**IWICFactory::CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer).</span></span> <span data-ttu-id="5748a-112">[**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)是裝置色彩設定檔的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="5748a-112">The [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) is an abstraction for device color profile.</span></span> <span data-ttu-id="5748a-113">**IWICColorCoNtext** 會以點陣圖框架、來源裝置的色彩設定檔和目標裝置的色彩設定檔進行初始化。</span><span class="sxs-lookup"><span data-stu-id="5748a-113">**IWICColorContext** is initialized with a bitmap frame, the color profile of the source device and the color profile of the target device.</span></span> <span data-ttu-id="5748a-114">它會執行點陣圖框架的轉換。</span><span class="sxs-lookup"><span data-stu-id="5748a-114">It performs the conversion of the bitmap frame.</span></span>

 

 



