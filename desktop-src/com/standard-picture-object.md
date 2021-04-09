---
title: 標準圖片物件
description: 標準圖片物件
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933642"
---
# <a name="standard-picture-object"></a><span data-ttu-id="b2a99-103">標準圖片物件</span><span class="sxs-lookup"><span data-stu-id="b2a99-103">Standard Picture Object</span></span>

<span data-ttu-id="b2a99-104">標準圖片物件提供 GDI 影像的非語言相關抽象概念：點陣圖、圖示、中繼檔和增強的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="b2a99-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="b2a99-105">就像標準字型物件一樣，系統會提供此物件的標準執行。</span><span class="sxs-lookup"><span data-stu-id="b2a99-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="b2a99-106">其主要介面為 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 和 [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)，後者衍生自 **IDispatch** ，以透過 OLE automation 提供圖片屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="b2a99-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="b2a99-107">使用 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)建立新的圖片物件。</span><span class="sxs-lookup"><span data-stu-id="b2a99-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="b2a99-108">圖片物件也支援輸出介面 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) ，讓用戶端可以決定圖片屬性變更的時間。</span><span class="sxs-lookup"><span data-stu-id="b2a99-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="b2a99-109">因此，圖片物件也支援 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 和一個 **IPropertyNotifySink** 的連接點。</span><span class="sxs-lookup"><span data-stu-id="b2a99-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="b2a99-110">Picture 物件也支援 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ，讓它可以從 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)實例儲存和載入本身。</span><span class="sxs-lookup"><span data-stu-id="b2a99-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="b2a99-111">在內部使用圖片物件的物件通常會在物件的持續性處理過程中，儲存並載入圖片。</span><span class="sxs-lookup"><span data-stu-id="b2a99-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="b2a99-112">[**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)函式會根據資料流程內容簡化圖片物件的建立。</span><span class="sxs-lookup"><span data-stu-id="b2a99-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2a99-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2a99-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2a99-114">控制項屬性</span><span class="sxs-lookup"><span data-stu-id="b2a99-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 