---
description: 自動資源回收
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: 自動資源回收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317892"
---
# <a name="automatic-resource-reclamation"></a>自動資源回收

COM + 會在每次物件的存留期結束時，通知分配器管理員。 然後，分配者管理員會通知每個已註冊的資源配置器的持有者，查看是否有此物件仍保留的任何資源。 如果是的話，就會釋出這些資源，藉由透過資源配置器取得資源的元件來避免資源流失的可能性。

自動回收功能是預設為關閉的選項。 資源配置器可以選擇啟用這個選項，而且在這樣做之後，物件方法絕對不會傳回對物件回傳之任何資源的參考。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



