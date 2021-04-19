---
description: 透過 WIA 腳本模型，Windows 映像取得 (WIA) 功能提供給指令碼語言，例如 Microsoft JScript 開發軟體和 Microsoft Visual Basic Scripting Edition (VBScript) ，以及 Microsoft Visual Basic 開發系統等高階語言。
ms.assetid: eec5dc91-7b32-4f38-bdfe-c11bddc17ba2
title: 使用 WIA 腳本模型
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: affa2c4368a83b2d67c1c6219b76040ba043a1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971009"
---
# <a name="using-the-wia-scripting-model"></a><span data-ttu-id="d9f96-103">使用 WIA 腳本模型</span><span class="sxs-lookup"><span data-stu-id="d9f96-103">Using the WIA Scripting Model</span></span>

<span data-ttu-id="d9f96-104">透過 [WIA 腳本模型](-wia-wia-scripting-model.md)，Windows 映像取得 (WIA) 功能提供給指令碼語言，例如 microsoft JScript 開發軟體和 microsoft Visual Basic Scripting Edition (VBScript) ，以及 microsoft Visual Basic 開發系統等高階語言。</span><span class="sxs-lookup"><span data-stu-id="d9f96-104">Through the [WIA Scripting Model](-wia-wia-scripting-model.md), Windows Image Acquisition (WIA) functionality is made available to scripting languages such as Microsoft JScript development software and Microsoft Visual Basic Scripting Edition (VBScript), and high-level languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="d9f96-105">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="d9f96-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="d9f96-106">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="d9f96-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="d9f96-107">WIA 腳本模型會公開繼承 [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="d9f96-107">The WIA scripting model exposes objects that inherit the [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

<span data-ttu-id="d9f96-108">腳本模型提供 WIAAPI 的簡化版本。</span><span class="sxs-lookup"><span data-stu-id="d9f96-108">The scripting model offers a simplified version of the WIAAPI.</span></span>

<span data-ttu-id="d9f96-109">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="d9f96-109">For more information, see the following:</span></span>

-   [<span data-ttu-id="d9f96-110">設定腳本模型開發環境</span><span class="sxs-lookup"><span data-stu-id="d9f96-110">Setting up the Scripting Model Development Environment</span></span>](-wia-setting-up-the-scripting-model.md)
-   [<span data-ttu-id="d9f96-111">連接至裝置</span><span class="sxs-lookup"><span data-stu-id="d9f96-111">Connecting to a Device</span></span>](-wia-connecting-to-a-device.md)
-   [<span data-ttu-id="d9f96-112">流覽專案物件的樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d9f96-112">Navigating a Tree of Item Objects</span></span>](-wia-navigating-a-tree-of-item-objects.md)
-   [<span data-ttu-id="d9f96-113">傳送資料</span><span class="sxs-lookup"><span data-stu-id="d9f96-113">Transferring Data</span></span>](-wia-transferring-data.md)
-   [<span data-ttu-id="d9f96-114">腳本模型的限制</span><span class="sxs-lookup"><span data-stu-id="d9f96-114">Limitations of the Scripting Model</span></span>](-wia-limitations-of-the-scripting-model.md)

 

 
