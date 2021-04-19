---
description: Windows 映像取得 (WIA) Api 會以 HRESULT 傳回值傳回其完成狀態。
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: WIA 錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971007"
---
# <a name="wia-error-information"></a>WIA 錯誤資訊

Windows 映像取得 (WIA) Api 會以 HRESULT 傳回值傳回其完成狀態。 應用程式會根據設備 WIA 常數來檢查這些傳回值 \_ ，以判斷錯誤是否需要使用者介入來清除（例如卡紙路徑），並將它們回報給使用者。 此外，所有驅動層級錯誤都會詳細記錄到事件記錄檔，並使用裝置迷你驅動程式提供的錯誤字串。 如需 WIA 特定錯誤碼的清單，請參閱 [錯誤碼](-wia-error-codes.md)。

 

 



