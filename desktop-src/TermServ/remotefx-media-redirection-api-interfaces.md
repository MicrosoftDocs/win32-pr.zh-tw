---
title: RemoteFX 媒體重新導向 API 介面
description: RemoteFX 媒體重新導向 API 支援下列介面。
ms.assetid: 9fb19c56-67a8-40f1-b6f1-8448eb83b38c
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed66bdeba9d554af4b9b42c74f4e4db95484f4c1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312747"
---
# <a name="remotefx-media-redirection-api-interfaces"></a><span data-ttu-id="57f16-103">RemoteFX 媒體重新導向 API 介面</span><span class="sxs-lookup"><span data-stu-id="57f16-103">RemoteFX Media Redirection API interfaces</span></span>

<span data-ttu-id="57f16-104">RemoteFX 媒體重新導向 API 支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="57f16-104">The RemoteFX media redirection API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="57f16-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="57f16-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="57f16-106">**IWTSBitmapRenderer**</span><span class="sxs-lookup"><span data-stu-id="57f16-106">**IWTSBitmapRenderer**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer)
</dt> <dd>

<span data-ttu-id="57f16-107">由動態虛擬通道外掛程式用來呈現點陣圖。</span><span class="sxs-lookup"><span data-stu-id="57f16-107">Used by a dynamic virtual channel plug-in to render bitmaps.</span></span>

</dd> <dt>

[<span data-ttu-id="57f16-108">**IWTSBitmapRendererCallback**</span><span class="sxs-lookup"><span data-stu-id="57f16-108">**IWTSBitmapRendererCallback**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderercallback)
</dt> <dd>

<span data-ttu-id="57f16-109">動態虛擬通道外掛程式會執行這個介面，以便在轉譯區域的大小變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="57f16-109">A dynamic virtual channel plug-in implements this interface to be notified when the size of the rendering area changes.</span></span>

</dd> <dt>

[<span data-ttu-id="57f16-110">**IWTSBitmapRenderService**</span><span class="sxs-lookup"><span data-stu-id="57f16-110">**IWTSBitmapRenderService**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderservice)
</dt> <dd>

<span data-ttu-id="57f16-111">這項服務是用來在用戶端上建立對應到伺服器上對應視窗的視覺化對應。</span><span class="sxs-lookup"><span data-stu-id="57f16-111">This service is used to create a visual mapping on the client corresponding to a mapped window on the server.</span></span>

</dd> <dt>

[<span data-ttu-id="57f16-112">**IWTSPluginServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="57f16-112">**IWTSPluginServiceProvider**</span></span>](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtspluginserviceprovider)
</dt> <dd>

<span data-ttu-id="57f16-113">提供一種方式，讓動態虛擬通道外掛程式查詢各種遠端桌面用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="57f16-113">Provides a way for Dynamic Virtual Channel plug-ins to query various Remote Desktop Client services.</span></span>

</dd> </dl>

 

 




