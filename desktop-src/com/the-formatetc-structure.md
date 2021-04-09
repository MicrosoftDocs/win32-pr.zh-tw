---
title: FORMATETC 結構
description: FORMATETC 結構是一般化剪貼簿格式，已增強以包含目標裝置、資料的外觀或觀點，以及儲存媒體。
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683168"
---
# <a name="the-formatetc-structure"></a><span data-ttu-id="fbdaf-103">FORMATETC 結構</span><span class="sxs-lookup"><span data-stu-id="fbdaf-103">The FORMATETC Structure</span></span>

<span data-ttu-id="fbdaf-104">FORMATETC 結構是一般化剪貼簿格式，已增強以包含目標裝置、資料的 *外觀* 或觀點，以及儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-104">The FORMATETC structure is a generalized clipboard format, enhanced to encompass a target device, an *aspect* or view of the data, and a storage medium.</span></span> <span data-ttu-id="fbdaf-105">資料取用者（例如 OLE 容器應用程式）會在對 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)的呼叫中將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構傳遞為引數，以表示它想要從資料來源（例如複合檔案物件）的資料類型。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-105">A data consumer, such as an OLE container application, passes the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure as an argument in calls to [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) to indicate the type of data it wants from a data source, such as a compound document object.</span></span> <span data-ttu-id="fbdaf-106">來源會使用 **FORMATETC** 結構來描述它可提供的格式。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-106">The source uses the **FORMATETC** structure to describe what formats it can provide.</span></span>

<span data-ttu-id="fbdaf-107">[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 可以描述幾乎所有資料，包括其他物件（例如，例如名字）。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-107">[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) can describe virtually any data, including other objects such as monikers.</span></span> <span data-ttu-id="fbdaf-108">容器可以呼叫 [**IDataObject：： EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)來要求其中一個内嵌物件來列出其資料格式，以傳回可執行 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 介面的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-108">A container can ask one of its embedded objects to list its data formats by calling [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), which returns an enumerator object that implements the [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) interface.</span></span> <span data-ttu-id="fbdaf-109">而不是只回復它有「文字和點陣圖」。物件可以提供資料的詳細說明，包括裝置 (通常呈現的螢幕或印表機) 、呈現給使用者的外觀 (完整的內容、縮圖、圖示或列印) 的格式，以及包含資料 (全域記憶體、磁片檔案、儲存物件或串流) 的儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-109">Instead of replying merely that it has "text and a bitmap," the object can provide a detailed description of the data, including the device (normally screen or printer) for which it is rendered, the aspect to be presented to the user (full contents, thumbnail, icon, or formatted for printing), and the storage medium containing the data (global memory, disk file, storage object, or stream).</span></span> <span data-ttu-id="fbdaf-110">這項能夠緊密描述資料的功能，會導致高品質的印表機和螢幕輸出，以及更有效率的資料流覽，其中縮圖草圖的抓取和顯示速度會比完整的呈現更快。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-110">This ability to tightly describe data will, in time, result in higher quality printer and screen output as well as more efficiency in data browsing, where a thumbnail sketch is much faster to retrieve and display than a fully detailed rendering.</span></span>

<span data-ttu-id="fbdaf-111">下表列出 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 資料結構的欄位，以及它們所指定的資訊。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-111">The following table lists fields of the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) data structure and the information that they specify.</span></span>



| <span data-ttu-id="fbdaf-112">欄位</span><span class="sxs-lookup"><span data-stu-id="fbdaf-112">Field</span></span>                   | <span data-ttu-id="fbdaf-113">指定</span><span class="sxs-lookup"><span data-stu-id="fbdaf-113">Specifies</span></span>                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbdaf-114">**cfFormat**</span><span class="sxs-lookup"><span data-stu-id="fbdaf-114">**cfFormat**</span></span><br/> | <span data-ttu-id="fbdaf-115">轉譯資料的格式，可以是標準剪貼簿格式、專屬格式或 OLE 格式。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-115">The format in which the data is to be rendered, which can be a standard clipboard format, a proprietary format, or an OLE format.</span></span> <span data-ttu-id="fbdaf-116">如需有關 OLE 格式的詳細資訊，請參閱 [複合檔案](compound-documents.md)。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-116">For more information on OLE formats, see [Compound Documents](compound-documents.md).</span></span><br/>                                          |
| <span data-ttu-id="fbdaf-117">**ptd**</span><span class="sxs-lookup"><span data-stu-id="fbdaf-117">**ptd**</span></span><br/>      | <span data-ttu-id="fbdaf-118">[**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice)結構，其中包含與 Windows 目標裝置相關的足夠資訊（例如螢幕或印表機），因此可以使用 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)函式來建立其裝置內容的控制碼 (hDC) 。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-118">A [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) structure, which contains enough information about a Windows target device, such as a screen or printer, so that a handle to its device context (hDC) can be created using the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span> <br/> |
| <span data-ttu-id="fbdaf-119">**dwAspect**</span><span class="sxs-lookup"><span data-stu-id="fbdaf-119">**dwAspect**</span></span><br/> | <span data-ttu-id="fbdaf-120">要呈現之資料的外觀或觀點;可以是完整的內容、縮圖草圖、圖示，或格式化以進行列印。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-120">The aspect or view of the data to be rendered; can be the full contents, a thumbnail sketch, an icon, or formatted for printing.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="fbdaf-121">**lindex**</span><span class="sxs-lookup"><span data-stu-id="fbdaf-121">**lindex**</span></span><br/>   | <span data-ttu-id="fbdaf-122">感興趣的層面部分;目前，此值必須是-1，表示會有興趣的整個觀點。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-122">The part of the aspect that is of interest; for the present, the value must be -1, indicating that the entire view is of interest.</span></span><br/>                                                                                                                                |
| <span data-ttu-id="fbdaf-123">**tymed**</span><span class="sxs-lookup"><span data-stu-id="fbdaf-123">**tymed**</span></span><br/>    | <span data-ttu-id="fbdaf-124">資料的儲存媒體，可以是全域記憶體、磁片檔案或其中一個 COM 結構儲存介面的實例。</span><span class="sxs-lookup"><span data-stu-id="fbdaf-124">The data's storage medium, which can be global memory, disk file, or an instance of one of COM's structured-storage interfaces.</span></span><br/>                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="fbdaf-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbdaf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbdaf-126">資料格式和傳輸媒體</span><span class="sxs-lookup"><span data-stu-id="fbdaf-126">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

