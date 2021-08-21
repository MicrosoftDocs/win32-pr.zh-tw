---
description: 地區設定傳回 \_ \* 常數
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466025"
---
# <a name="locale_return-constants"></a>地區設定傳回 \_ \* 常數

本主題定義 NLS 所使用的地區設定傳回 \_ \* 常數。




| 值 | 意義 | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 和更新版本：</strong>取出月份的所有格名稱，這些名稱是月份名稱與其他專案合併時所使用的名稱。 例如，在「烏克蘭」中，當月份單獨命名時，1月的對等專案會寫入「Січень」。 不過，當月份名稱用於組合時（例如，在2003年1月5日的日期）中，會使用名稱的所有格形式。 針對烏克蘭範例，所有格月份名稱會顯示為 "5 січня 2003"。 所有格月份名稱的清單會從1月開始，並以分號分隔。 如果沒有13個月，請在清單結尾使用分號。<blockquote>[!Note]<br />所有語言都不會有所有格的月份名稱。</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98，Windows NT 4.0 和更新版本：</strong>取出數位。 這個常數會造成 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> 或 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> 以數位形式（而不是字串）來取出值。 接收值的緩衝區必須至少為 DWORD 值的長度。 這個常數可以與名稱開頭為 "LOCALE_I" 的任何其他常數合併。 | 




 

 

 




