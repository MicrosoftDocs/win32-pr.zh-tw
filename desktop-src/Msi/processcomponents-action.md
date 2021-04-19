---
description: ProcessComponents 動作會註冊及取消註冊元件、其金鑰路徑和元件用戶端。
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: ProcessComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985289"
---
# <a name="processcomponents-action"></a>ProcessComponents 動作

ProcessComponents 動作會註冊及取消註冊元件、其金鑰路徑和元件用戶端。 ProcessComponents 動作會查詢 [元件資料表](component-table.md) 的 KeyPath 資料行，以判斷 keypaths。 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)會使用此註冊來傳回產品用戶端元件的路徑。

## <a name="sequence-restrictions"></a>順序限制

ProcessComponents 動作必須晚于 [InstallInitialize](installinitialize-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息

針對每個註冊的元件。



| 欄位 | 動作資料的描述      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentId                     |
| \[3\] | 元件的金鑰路徑。 |



 

針對正在取消註冊的每個元件。



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentId                |



 

 

 



