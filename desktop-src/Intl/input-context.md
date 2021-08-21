---
description: '&\# 0034; 輸入內容&\# 0034; 是由 IMM 維護的內部結構。'
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: 輸入內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2927d3f573704aadb1ef72bdb26a35d37d90c1f90ab58d3a947ee84f8f38f7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145897"
---
# <a name="input-context"></a>輸入內容

「輸入內容」是由 IMM 維護的內部結構。 它包含 IME 狀態的相關資訊，並由 IME 視窗使用。 根據預設，作業系統會建立並指派輸入內容到每個執行緒。 線上程中，此預設輸入內容是共用資源，並與每個新建立的視窗相關聯。

若要在 IME 中取得或設定資訊，IME 感知的應用程式必須先取得與指定視窗相關聯之輸入內容的控制碼。 應用程式會使用 [**ImmGetCoNtext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) 函數來抓取控制碼。 它可以在後續呼叫的 IMM 函式中使用抓取的控制碼，以抓取和設定 IME 值，例如撰寫視窗樣式、撰寫樣式和狀態視窗位置。 應用程式使用完內容之後，就必須使用 [**ImmReleaseCoNtext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) 函式來釋放內容。

由於預設輸入內容是共用資源，因此應用程式對其進行的任何變更都會套用至執行緒中的所有視窗。 不過，應用程式可以藉由建立自己的輸入內容，並將它與執行緒的一或多個視窗產生關聯，來覆寫這個預設行為。 對應用程式特定輸入內容所做的變更只會套用至與內容相關聯的視窗。

您的應用程式可以使用 [**ImmCreateCoNtext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) 函數來建立輸入內容。 若要將內容指派給視窗，應用程式會呼叫 [**ImmAssociateCoNtext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) 函數。 此函式會將控制碼傳回至先前關聯的輸入內容。 如果應用程式尚未與視窗建立關聯的輸入內容，傳回的控制碼會是預設的輸入內容。 一般來說，當不再需要自訂的輸入內容時，應用程式會儲存此控制碼，並在稍後使用視窗重新關聯它。

一旦輸入內容與視窗相關聯之後，作業系統會在視窗啟動時自動選取該內容，並接收輸入焦點。 輸入內容中的樣式和其他資訊會影響該視窗的後續鍵盤輸入，以判斷 IME 的運作方式。

您的應用程式必須在結束之前終結任何自訂的輸入內容。 首先，應用程式會使用 [**ImmAssociateCoNtext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) 函式，從線上程中與 windows 建立的任何關聯中移除輸入內容。 然後，它會呼叫 [**ImmDestroyCoNtext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於輸入方法管理員](about-input-method-manager.md)
</dt> </dl>

 

 



