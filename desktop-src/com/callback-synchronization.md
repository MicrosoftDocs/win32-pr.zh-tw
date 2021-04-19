---
title: 回呼同步處理
description: 回呼同步處理
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106978586"
---
# <a name="callback-synchronization"></a>回呼同步處理

非同步 [WININET API](/windows/desktop/WinInet/portal) (用於最常見的通訊協定) 讓回呼機制和呼叫應用程式的同步處理成為用戶端的練習。 這是故意的，因為它允許最大程度的彈性。 預設的通訊協定和 URL 的標記執行會執行這種同步處理，並保證單一執行緒和執行緒應用程式永遠不需要處理無限制執行緒的爭用。 也就是說，用戶端的 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 和 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面只會在其適當的執行緒上呼叫。 這項功能對於 URL mMoniker 的使用者而言是透明的，只要呼叫 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 和 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 的每個執行緒都有訊息佇列。

非同步「標記」規格需要更精確地控制下載的優先順序與管理，而不是 WinSock 或 WinInet 所允許的。 因此，URL 標記會針對任何指定的呼叫端執行緒管理所有下載，並使用 (作為其同步處理的一部分，) 以 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) 規格為基礎的優先順序配置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[URL 的名字](url-monikers.md)
</dt> </dl>

 

 