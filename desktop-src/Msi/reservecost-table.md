---
description: ReserveCost 資料表是選擇性的表格，可讓作者保留任何目錄中的磁碟空間量，而這些目錄相依于元件的安裝狀態。
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: ReserveCost 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944478"
---
# <a name="reservecost-table"></a>ReserveCost 資料表

ReserveCost 資料表是選擇性的表格，可讓作者保留任何目錄中的磁碟空間量，而這些目錄相依于元件的安裝狀態。

ReserveCost 資料表具有下列資料行。



| Column        | 類型                               | 答案 | Nullable |
|---------------|------------------------------------|-----|----------|
| ReserveKey    | [識別碼](identifier.md)       | Y   | N        |
| 元件\_   | [識別碼](identifier.md)       | N   | N        |
| ReserveFolder | [識別碼](identifier.md)       | N   | Y        |
| ReserveLocal  | [DoubleInteger](doubleinteger.md) | N   | N        |
| ReserveSource | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey
</dt> <dd>

可唯一識別 ReserveCost 資料表專案的主鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件](component-table.md)資料表中第一個資料行的外部索引鍵。 如果要安裝此元件，則保留指定的空間量。

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

此資料行包含的屬性名稱是目的地目錄的完整路徑。 這個屬性名稱通常是 [目錄](directory-table.md) 資料表中的目錄名稱，或使用 [Appsearch](appsearch-action.md) 動作所取得之屬性集的名稱。 這會將 ReserveLocal 或 ReserveSource 中指定的磁碟空間量新增至包含目錄之裝置的磁片區成本。

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

當連結的元件安裝在本機執行時，所要保留的磁碟空間位元組數目。

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource
</dt> <dd>

當連結的元件安裝成從來源執行時，所要保留的磁碟空間位元組數目。

</dd> </dl>

## <a name="remarks"></a>備註

以這種方式保留成本可能適合想要確保在安裝完成之後可使用最少磁碟空間的作者。 例如，此磁碟空間可能會保留給使用者檔或應用程式檔 (例如，只有在安裝之後啟動應用程式時才會建立的索引檔案) 。

您可以使用 ReserveCost 資料表來啟用自訂動作，以指定自訂動作可能會安裝之任何檔案、登錄專案或其他專案的大約成本。 將專案加入至 ReserveCost 資料表的自訂動作應該在 [CostInitialize](costinitialize-action.md) 和 [FileCost](filecost-action.md) 動作之間排序。 這是 FileCost 動作的必要專案，可正確地初始化受 ReserveCost 資料表中專案影響的所有元件的成本。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



