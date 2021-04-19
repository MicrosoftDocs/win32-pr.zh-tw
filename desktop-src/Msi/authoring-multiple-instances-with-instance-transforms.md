---
description: 若要從一個 Windows Installer 套件安裝產品的多個實例，您必須撰寫產品的基底安裝套件，以及要安裝的每個實例的實例轉換，以及基底實例。
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: 使用實例轉換撰寫多個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977873"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>使用實例轉換撰寫多個實例

若要從一個 Windows Installer 套件安裝產品的多個實例，您必須撰寫產品的基底安裝套件，以及要安裝的每個實例的實例轉換，以及基底實例。 撰寫基底套件和轉換時，請使用下列指導方針：

-   您的安裝應用程式可以檢查 Windows Vista、Windows Server 2003、Windows XP Service Pack 1 (SP1) 和 Windows Installer 3.0 可轉散發套件上執行的安裝程式是否存在。  (或更新版本) 的任何安裝程式版本都必須使用產品程式碼-變更轉換，從單一套件安裝多個實例。
-   每個實例都必須有唯一的產品代碼和實例識別碼。 您可以在基底封裝中定義屬性，其值可以設定為實例識別碼。
-   為了讓每個實例的檔案保持隔離，基底封裝應該將檔案安裝到相依于實例識別碼的目錄位置。
-   為了讓每個實例的非資料保持隔離，基底封裝應該將非資料的資料收集到每個實例的元件集合中。 接著應根據相依于實例識別碼的條件陳述式來安裝適當的元件。
-   除了基底實例之外，還會針對每個要安裝的實例撰寫實例轉換。 基底套件可能會安裝自己的實例。
-   實例轉換必須變更每個實例的產品代碼和識別碼。
-   建議產品轉換也會變更產品名稱，以便透過主控台在 [新增/移除程式] 中輕鬆分辨實例。
-   如果實例轉換會安裝檔案，它們應該安裝在相依于實例識別碼的目錄中。
-   所有非資料（例如登錄機碼）都應該在其路徑中包含實例名稱，以避免發生衝突。 您可以使用其值為路徑中實例識別碼的屬性來完成這項作業，如下列登錄 [表](registry-table.md)範例所示。



| 登錄 | Root | 按鍵                                            | 名稱         | 值           | 元件\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

如需詳細資訊，請參閱 [安裝多個產品的實例和修補程式](installing-multiple-instances-of-products-and-patches.md) ，以及 [使用實例轉換來安裝多個實例](installing-multiple-instances-with-instance-transforms.md)。

 

 



