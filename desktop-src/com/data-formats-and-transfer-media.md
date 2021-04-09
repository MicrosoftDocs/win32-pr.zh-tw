---
title: 資料格式和傳輸媒體
description: 資料格式和傳輸媒體
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104024315"
---
# <a name="data-formats-and-transfer-media"></a>資料格式和傳輸媒體

大部分的平臺（包括 Windows）都會根據一組稱為「剪貼簿」的函式，定義在應用程式之間傳輸資料的標準通訊協定。 使用這些函式的應用程式即使其原生資料格式截然不同，也可以共用資料。 一般而言，這些寫字板有兩個嚴重的缺點，也就是 COM 所克服的。

首先，資料描述只會使用格式識別碼，例如 Windows 上的單一16位剪貼簿格式識別碼，這表示剪貼簿只能描述其資料的結構，也就是位的順序。 它可以報告「我有點陣圖」或「我有一些文字」，但它無法指定用來組成資料的目標裝置、資料可提供的觀點或本身，或是哪一個儲存體媒體最適合其傳輸。 例如，它無法回報：「我有一串儲存在全域記憶體中的文字，並格式化為在螢幕或印表機上進行簡報」或「我有針對 100 DPI 點矩陣印表機呈現的縮圖草圖點陣圖，並儲存為磁片檔案。」

其次，使用剪貼簿的所有資料傳輸通常都是透過全域記憶體進行。 針對少量的資料，使用全域記憶體相當有效率，但郵差先生大很低，例如 20 MB 多媒體物件。 針對大型資料物件，全域記憶體的速度很慢，其大小需要大量交換至磁片上的虛擬記憶體。 如果要交換的資料通常會放在磁片上，則透過此虛擬記憶體瓶頸強制執行，將會產生效率不佳的情況。 更好的方法是完全略過全域記憶體，只是直接將資料傳輸到磁片。

為了減輕這些問題，COM 提供兩種資料結構： [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 和 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)。 如需詳細資訊，請參閱下列主題：

-   [FORMATETC 結構](the-formatetc-structure.md)
-   [STGMEDIUM 結構](the-stgmedium-structure.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料轉送](data-transfer.md)
</dt> </dl>

 

 




