---
description: 根據登錄資訊的類型，使用合併模組登錄表。
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: 撰寫合併模組登錄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03726481905d4efee2405d0b383f53833d840090fea74e2d41fc6ae67a8e5bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066148"
---
# <a name="authoring-merge-module-registry-tables"></a>撰寫合併模組登錄資料表

根據登錄資訊的類型，使用合併模組登錄表。

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>TypeLib、Class、AppId、ProgId、Extension、Verb 或 MIME 資料表

針對型別程式庫、類別、延伸模組和動詞，將登錄資訊撰寫至合併模組的 [TypeLib](typelib-table.md)、 [類別](class-table.md)、 [AppId](appid-table.md)、 [ProgId](progid-table.md)、 [擴充](extension-table.md)、 [動詞](verb-table.md)或 [MIME](mime-table.md) 資料表中。 如果您使用登錄[資料表](registry-table.md)來新增這項資訊，Windows 2000 無法針對這些元件提供整個系統的公告。

合併模組作者可能會因為下列原因而決定不使用類別表進行註冊：

-   若要由類別資料表註冊，檔案必須是其元件的 KeyPath。 這可能需要元件組織中的無法接受變更。
-   COM 呼叫可能會觸發安裝程式嘗試重新安裝已公告的類別。 作者可以決定不要使用類別表註冊類別，以避免在用戶端電腦不支援使用者介面時觸發重新安裝。

## <a name="registry-table"></a>登錄資料表

使用登錄資料表來加入無法撰寫到 TypeLib、類別、AppId、ProgId、延伸模組、動詞或 MIME 資料表的登錄資訊。 Windows 2000 無法針對使用登錄表的元件提供整個系統的公告。

編寫登錄表時，請參閱使用檔案的檔案路徑 \[ \# \] 或 \[ ！檔 \] 格式，而不是 \[ 目錄 \] 檔案名。 後者的格式不支援從來源執行安裝。 先前的格式也會讓遺失的檔案和錯誤的元件更容易偵測。

在登錄表的索引鍵資料行中使用格式化文字時，需要注意。 因為 Windows Installer 不會重新安裝已安裝的元件，所以使用此欄位中格式化的文字可能會導致在移除應用程式時留下登錄機碼。

## <a name="selfreg-table"></a>SelfReg 資料表

不建議使用 SelfReg 資料表。 如需不使用自我註冊的原因清單，請參閱 [SelfReg 資料表](selfreg-table.md)。 在其他所有情況下，您應該盡可能使用 TypeLib、Class、AppId、ProgId、Extension、Verb 和 MIME 資料表，以及登錄資料表。

 

 



