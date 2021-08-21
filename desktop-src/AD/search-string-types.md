---
title: 初始、中詞和最終搜尋字串
description: 在檔中，有三種類型的萬用字元搜尋可參考結構搜尋字串查詢。 這些萬用字元搜尋為初始、中式和最後搜尋的字串。 本主題說明這些搜尋。
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39547116846cad4d75a1fd9ae1998e602a8084912965a3dd269803c86845cefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024966"
---
# <a name="initial-medial-and-final-search-strings"></a>初始、中詞和最終搜尋字串

在檔中，有三種類型的萬用字元搜尋可參考結構搜尋字串查詢。 這些萬用字元搜尋是：初始、中的字串和最終搜尋字串。 本主題說明這些搜尋。

## <a name="initial-search-strings"></a>初始搜尋字串

初始搜尋字串會比對字串開頭的一組指定的字元，後面接著萬用字元。 例如，初始搜尋字串 `Act*` 會符合 "Active Directory"。

## <a name="medial-search-strings"></a>Medial-Search 字串

中間字元搜尋字串會比對字串中間的一組指定的字元，並在前面加上/或後面加上萬用字元。 中間詞搜尋字串 `*Dir*` 、 `*ive*Dir*` 和 `*ve*Dir*tor*` 都會符合 "Active Directory"。

## <a name="final-search-strings"></a>最終搜尋字串

最終搜尋字串會比對字串結尾的一組指定字元，並在前面加上萬用字元。 例如，最終搜尋字串 `*ory` 會符合 "Active Directory"。

 

 




