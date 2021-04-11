---
title: 使用 >idirectorysearch 的伺服器時間限制
description: 若要避免使用所有的 CPU 時間，並防止其他作業執行，請指定較小值的搜尋時間限制，然後稍後在無法產生報表時重新執行應用程式。
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 的伺服器時間限制
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、伺服器時間限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931826"
---
# <a name="server-time-limit-with-idirectorysearch"></a>使用 >idirectorysearch 的伺服器時間限制

當您在忙碌的伺服器上要求搜尋時，您可能會想要要求伺服器將搜尋限制在指定的時間限制。 例如，您想要執行應用程式，以在其容量接近的伺服器上產生每週報表。 若要避免使用所有的 CPU 時間，並防止其他作業執行，請指定較小值的搜尋時間限制，然後稍後在無法產生報表時重新執行應用程式。

有些伺服器可能會強加自己的系統管理時間限制。 在這些情況下，如果您指定的搜尋時間限制值大於管理時間限制，伺服器將會忽略您的規格，並改為使用其內部時間限制值。

伺服器時間限制的預設值為 [無限制]。 若要設定伺服器時間限制，請將 **ads \_ SEARCHPREF \_ time \_ limit** 搜尋選項設定為 **ADSTYPE \_ 整數** 值，其中包含傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中的伺服器時間限制（以秒為單位）。 下列程式碼範例會顯示這項作業。 伺服器時間限制為0表示沒有時間限制。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




