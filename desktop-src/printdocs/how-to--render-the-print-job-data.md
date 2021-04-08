---
description: 本主題說明如何呈現要列印的程式資料。
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 如何：轉譯列印工作資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852416"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="ce17e-103">如何：轉譯列印工作資料</span><span class="sxs-lookup"><span data-stu-id="ce17e-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="ce17e-104">本主題說明如何呈現要列印的程式資料。</span><span class="sxs-lookup"><span data-stu-id="ce17e-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="ce17e-105">本主題不會詳細說明如何呈現特定圖形或文字影像。</span><span class="sxs-lookup"><span data-stu-id="ce17e-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="ce17e-106">相反地，它會說明如何管理程式資料，並將其轉譯為 XPS 檔，以使用 [Xps 列印 API](xps-printing.md)傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="ce17e-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="ce17e-107">概觀</span><span class="sxs-lookup"><span data-stu-id="ce17e-107">Overview</span></span>

<span data-ttu-id="ce17e-108">轉譯列印工作資料以進行列印時，需要取得程式專屬的資料，例如文字、影像和格式，以及將其轉換成與目的地印表機相容的格式。</span><span class="sxs-lookup"><span data-stu-id="ce17e-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="ce17e-109">將資料傳送至印表機的程式必須以印表機驅動程式所需的格式來傳送。</span><span class="sxs-lookup"><span data-stu-id="ce17e-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="ce17e-110">使用 [Xps 列印 API](xps-printing.md) 將資料傳送至印表機，而且需要將資料格式化為 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="ce17e-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="ce17e-111">若要產生 XPS 列印 API 所需的 XPS 檔內容，範例程式會使用 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ce17e-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="ce17e-112">如果程式內容的格式與印表機不相容，則必須在將其傳送至印表機之前先轉譯。</span><span class="sxs-lookup"><span data-stu-id="ce17e-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="ce17e-113">如果程式使用 [XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85)) 來管理其程式內容，則程式內容會採用可直接傳送到 [XPS 列印 API](xps-printing.md) 的格式，而且在您將它傳送至印表機之前，不需要任何額外的轉譯。</span><span class="sxs-lookup"><span data-stu-id="ce17e-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce17e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce17e-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ce17e-115">[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ce17e-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ce17e-116">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="ce17e-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
