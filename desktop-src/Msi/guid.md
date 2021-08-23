---
description: GUID 資料類型是一種文字字串，代表 (識別碼) 的類別識別碼。 COM 必須能夠將字串轉換成有效的類別識別碼。 所有 Guid 都必須以大寫撰寫。
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: 'GUID (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e92688e11d71a51c59a2edc6c3e50ed01ab246c83bf4cfb9ac67b8d6318766b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649338"
---
# <a name="guid"></a>GUID

GUID 資料類型是一種文字字串，代表 (識別碼) 的類別識別碼。 COM 必須能夠將字串轉換成有效的類別識別碼。 所有 Guid 都必須以大寫撰寫。

GUID 的有效格式是 {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}，其中 X 是十六進位數位 (0、1、2、3、4、5、6、7、8、9、A、B、C、D、E、F) 。

請注意，GUIDGEN 之類的公用程式可以產生包含小寫字母的 Guid。 這些必須全部變更為大寫字母，安裝程式才能使用 GUID 做為有效的產品代碼、封裝碼或元件程式碼。

 

 



