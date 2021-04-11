---
description: TSPI 中使用不透明的控制碼來參考代表線條、電話和呼叫外觀的資料結構。
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: 不透明的控制碼和私用資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943599"
---
# <a name="opaque-handles-and-private-data-structures"></a>不透明的控制碼和私用資料結構

TSPI 中使用不透明的控制碼來參考代表線條、電話和呼叫外觀的資料結構。 這些會顯示為大部分函式和回呼的參數。 有幾個函式是使用裝置識別碼來參考裝置，而不是不透明的控制碼。 在這種情況下，參考會指向裝置本身，而不是資料結構。 以這種方式運作的函式通常是在建立資料結構和交換不透明的控制碼之前，于早期初始化時間呼叫的函數。

服務提供者必須決定如何解讀這些控制碼。 服務提供者通常會使用其資料結構的指標，或使用資料結構陣列中的索引做為不透明的控制碼。 唯一的限制是服務提供者不能使用值0做為 [HDRVLINE](hdrvline.md)、HDRVCALL 或 [HDRVPHONE](hdrvphone.md)。 控制碼的值0或 **Null** 在某些作業中具有特殊意義。

 

 



