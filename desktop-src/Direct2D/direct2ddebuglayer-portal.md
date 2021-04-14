---
title: Direct2D Debug 圖層
description: Direct2D 的執行時間延伸模組，可提供描述性的錯誤訊息、物件流失偵測、效能注意事項，以及協助您建立 Direct2D 應用程式的其他提示。
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371927"
---
# <a name="direct2d-debug-layer"></a>Direct2D Debug 圖層

## <a name="purpose"></a>目的

Direct2D debug 層會在其本身 DLL 中的 Direct2D （名為 d2d1debug.dll）分開執行，提供設計階段的偵測訊息，讓您可以將執行時間應用程式失敗降至最低。 偵測到的訊息通常是因為違反 API 合約的結果（例如無效參數） (可能是 Direct3D 相關) 、不正確資源、執行緒違規和其他效能問題，例如在剪輯足夠時使用圖層。

為了協助您決定 debug 層所追蹤的資訊數量，debug 層提供三個 debug 層級：資訊、警告和錯誤。 這三個層級的解讀方式如下：

-   **錯誤：** Direct2D 會將嚴重的錯誤訊息傳送至 debug 層。 例如，中斷線程條件約束將會產生嚴重的錯誤。

    此外，層級錯誤訊息會觸發中斷點，以協助您進行調試。

-   **警告：** Direct2D 會將錯誤訊息和警告傳送至 debug 圖層，以便您可以處理這些訊息。

-   **資訊：** Direct2D 會將錯誤訊息、警告和其他診斷資訊傳送至 debug 圖層。 例如，效能改進訊息將會在這個 debug 層級傳送。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [安裝 Direct2D Debug Layer](installing-the-direct2d-debug-layer.md)<br/> | 說明如何安裝 Direct2D debug 圖層。<br/>      |
| [Direct2D Debug 圖層總覽](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Debug 訊息](direct2ddebuglayer-debugmessages.md)<br/>                         | 列出來自 Direct2D Debug 層的 debug 訊息。<br/> |



 

 

 





