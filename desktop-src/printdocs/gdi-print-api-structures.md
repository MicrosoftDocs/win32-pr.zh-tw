---
description: GDI 列印 API 結構
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: GDI 列印 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ae427af0112061e6b90afa71cc2b65427d477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984604"
---
# <a name="gdi-print-api-structures"></a><span data-ttu-id="f0325-103">GDI 列印 API 結構</span><span class="sxs-lookup"><span data-stu-id="f0325-103">GDI Print API Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0325-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="f0325-104">In this section</span></span>



| <span data-ttu-id="f0325-105">結構</span><span class="sxs-lookup"><span data-stu-id="f0325-105">Structure</span></span>                                                      | <span data-ttu-id="f0325-106">Description</span><span class="sxs-lookup"><span data-stu-id="f0325-106">Description</span></span>                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0325-107">**版**</span><span class="sxs-lookup"><span data-stu-id="f0325-107">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | <span data-ttu-id="f0325-108">[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)資料結構包含有關印表機或顯示裝置之初始化和環境的資訊。</span><span class="sxs-lookup"><span data-stu-id="f0325-108">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure contains information about the initialization and environment of a printer or a display device.</span></span> <br/>                                                                                                              |
| [<span data-ttu-id="f0325-109">**DOCINFO**</span><span class="sxs-lookup"><span data-stu-id="f0325-109">**DOCINFO**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | <span data-ttu-id="f0325-110">[**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa)結構包含 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)函數所使用的輸入和輸出檔案名以及其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f0325-110">The [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure contains the input and output file names and other information used by the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) function.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="f0325-111">**DRAWPATRECT**</span><span class="sxs-lookup"><span data-stu-id="f0325-111">**DRAWPATRECT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | <span data-ttu-id="f0325-112">[**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect)結構會定義要建立的矩形。</span><span class="sxs-lookup"><span data-stu-id="f0325-112">The [**DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) structure defines a rectangle to be created.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="f0325-113">**PSFEATURE \_ CUSTPAPER**</span><span class="sxs-lookup"><span data-stu-id="f0325-113">**PSFEATURE\_CUSTPAPER**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | <span data-ttu-id="f0325-114">[**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper)結構包含 PostScript 驅動程式之自訂紙張大小的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0325-114">The [**PSFEATURE\_CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) structure contains information about a custom paper size for a PostScript driver.</span></span> <span data-ttu-id="f0325-115">此結構可搭配 [**GET \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) 印表機 escape 函式使用。</span><span class="sxs-lookup"><span data-stu-id="f0325-115">This structure is used with the [**GET\_PS\_FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) printer escape function.</span></span><br/> |
| [<span data-ttu-id="f0325-116">**PSFEATURE \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="f0325-116">**PSFEATURE\_OUTPUT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | <span data-ttu-id="f0325-117">[**PSFEATURE \_ 輸出**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output)結構包含 PostScript 驅動程式輸出選項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0325-117">The [**PSFEATURE\_OUTPUT**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) structure contains information about PostScript driver output options.</span></span> <span data-ttu-id="f0325-118">此結構可搭配 [**GET \_ PS \_ FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) 印表機 escape 函式使用。</span><span class="sxs-lookup"><span data-stu-id="f0325-118">This structure is used with the [**GET\_PS\_FEATURESETTING**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85)) printer escape function.</span></span><br/>                  |
| [<span data-ttu-id="f0325-119">**PSINJECTDATA**</span><span class="sxs-lookup"><span data-stu-id="f0325-119">**PSINJECTDATA**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | <span data-ttu-id="f0325-120">[**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata)結構是搭配 [**POSTSCRIPT \_ 插入**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85))印表機 escape 函式使用之輸入緩衝區的標頭。</span><span class="sxs-lookup"><span data-stu-id="f0325-120">The [**PSINJECTDATA**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) structure is a header for the input buffer used with the [**POSTSCRIPT\_INJECTION**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85)) printer escape function.</span></span><br/>                                                                            |



 

 

