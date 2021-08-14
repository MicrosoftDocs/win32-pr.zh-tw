---
description: 每個 Active Directory 物件都有指派的安全描述項。
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: 目錄服務存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913761"
---
# <a name="directory-services-access-rights"></a>目錄服務存取權限

每個 Active Directory 物件都有指派的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 。 您可以在這些安全描述項中設定一組目錄服務物件專屬的信任者許可權。 下表列出這些許可權。 如需詳細資訊，請參閱 [控制存取權限](/windows/desktop/AD/control-access-rights)。



| 權限                                | 意義                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 開啟的 ACTRL \_ DS \_<br/>            | 開啟 DS 物件。<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ 建立 \_ 子系<br/>   | 建立子 DS 物件。<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ 刪除 \_ 子系<br/>   | 刪除子 DS 物件。<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ 清單<br/>            | 列舉 DS 物件。<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ 讀取 \_ 的<br/>      | 讀取 DS 物件的屬性。<br/>                                                                                                                                                                                                                                          |
| ACTRL \_ DS \_ 寫入 \_<br/>     | 寫入 DS 物件的屬性。<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ 自助<br/>            | 只有在執行物件支援的已驗證許可權檢查之後，才允許存取。 您可以單獨使用此旗標來執行物件的所有已驗證許可權檢查，也可以結合特定驗證許可權的識別碼來執行該檢查。<br/> |
| ACTRL \_ DS \_ 刪除 \_ 樹狀結構<br/>    | 刪除 DS 物件的樹狀結構。<br/>                                                                                                                                                                                                                                                 |
| ACTRL \_ DS \_ 清單 \_ 物件<br/>    | 列出 DS 物件的樹狀結構。<br/>                                                                                                                                                                                                                                                   |
| ACTRL \_ DS \_ 控制 \_ 存取<br/> | 只有在執行物件支援的延伸許可權檢查之後，才允許存取。 您可以單獨使用此旗標來執行物件上的所有擴充許可權檢查，或結合特定擴充許可權的識別碼來執行該檢查。<br/>    |



 

 

