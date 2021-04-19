---
description: 說明如何建立憑證要求，並在憑證存放區中接收和儲存傳回的憑證。
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: 使用憑證註冊控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac3da319571b164fe66eb5bb3ac647c2978fff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993005"
---
# <a name="using-certificate-enrollment-control"></a>使用憑證註冊控制項

憑證註冊控制項是具有許多屬性和數種方法的單一物件，可用來判斷憑證註冊控制項處理使用者資訊的方式、要要求的憑證類型、產生金鑰的方式、要儲存的憑證，以及相關的進程。 憑證註冊控制項有兩種主要用途：建立 (PKCS 10) 的 [*憑證要求*](../secgloss/c-gly.md) \# ，以及接收傳回的憑證並將其儲存在 [*憑證存放區*](../secgloss/c-gly.md)中。 如需建立憑證註冊控制項物件的實例、設定其屬性，以及使用其方法的詳細資訊和語法，請參閱下列主題。



| 資訊                                                                                                                                                                                           | 主題                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 以不同的程式設計語言建立憑證註冊控制物件的實例                                                                                                  | [建立憑證註冊控制項物件的實例](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| 使用不同程式設計語言的憑證註冊控制項屬性                                                                                                                    | [使用憑證註冊控制項屬性](using-the-certificate-enrollment-control-properties.md)                             |
| 收集必要的資訊，並以不同的程式設計語言提交 [*憑證要求*](../secgloss/c-gly.md) 。 | [建立憑證要求](creating-the-certificate-request.md)                                                                   |
| 解壓縮和儲存已完成的憑證                                                                                                                                                      | [接收傳回的憑證](receiving-the-returned-certificate.md)                                                               |
| 從不同語言的傳回值中取出資訊                                                                                                                                      | [方法傳回值](method-return-values.md)                                                                                           |
| 檢查錯誤                                                                                                                                                                                   | [錯誤檢查](error-checking.md)                                                                                                       |



 

 

 
