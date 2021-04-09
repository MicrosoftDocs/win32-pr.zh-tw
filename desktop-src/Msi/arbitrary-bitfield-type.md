---
description: '&\# 0034;位&\# 0034; 沒有內容要求的類型，使用者提供的整數值是用來設定位中的一或多個位。 這段文字可能是與資料庫字碼頁相容的任何語言。'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: 任意位欄位類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115380"
---
# <a name="arbitrary-bitfield-type"></a>任意位欄位類型

沒有內容要求的 "bit" 類型，使用者提供的整數值是用來設定位中的一或多個位。 這段文字可能是與資料庫字碼頁相容的任何語言。

[語義類型](semantic-types.md)的任意位欄位類型是其中一個位欄位類型。 此類型是由使用者從一組選擇所選擇的整數所組成。 合併工具會將選取的整數取代為 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 [值] 資料行中所指定的範本。 若要指定此類型的可設定專案，模組作者應該在 [名稱] 資料行中輸入專案的名稱，在 [格式] 資料行中輸入 "3"，將類型資料行保留空白，並在 [ModuleConfiguration 資料表](moduleconfiguration-table.md)的 CoNtextData 資料行中輸入可能的整數清單。

類型資料行是保留的，而且必須是 null。 所有欄位類型的 CoNtextData 資料行中的專案都必須採用 ";" 格式 <mask> 。<Name>=<value>;<Name>=<value>... "，其中 <mask> 是一個整數值，指出感興趣的位、 <Name> 可當地語系化的顯示名稱，以及 <value> 這是十進位整數值。 內容資料行使用中的 [CMSM 特殊格式](cmsm-special-format.md) 和所有等位類型。 您可以在欄位中輸入常值 "=" 或 ";" 字元，方法是在 <Name> 該字元前面加上反斜線 ( ' \\ ' ) 字元。

 

 



