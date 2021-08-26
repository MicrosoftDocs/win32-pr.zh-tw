---
description: Windows 影像取得 (WIA) api 會以 HRESULT 傳回值傳回其完成狀態。
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: WIA 錯誤資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056958"
---
# <a name="wia-error-information"></a>WIA 錯誤資訊

Windows 影像取得 (WIA) api 會以 HRESULT 傳回值傳回其完成狀態。 應用程式會根據設備 WIA 常數來檢查這些傳回值 \_ ，以判斷錯誤是否需要使用者介入來清除（例如卡紙路徑），並將它們回報給使用者。 此外，所有驅動層級錯誤都會詳細記錄到事件記錄檔，並使用裝置迷你驅動程式提供的錯誤字串。 如需 WIA 特定錯誤碼的清單，請參閱 [錯誤碼](-wia-error-codes.md)。

 

 



