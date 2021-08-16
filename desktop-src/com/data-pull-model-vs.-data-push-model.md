---
title: Data-Pull 模型和 Data-Push 模型
description: Data-Pull 模型和 Data-Push 模型
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab89f61301f9116a7e826f1965bd54f75004a3a90af8c9d1a1bc13acb1fc9c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048446"
---
# <a name="data-pull-model-and-data-push-model"></a>Data-Pull 模型和 Data-Push 模型

非同步標記的用戶端可以在資料提取和資料推送模型之間進行選擇，以驅動非同步 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 作業並接收非同步通知。 在資料提取模型中，用戶端會驅動系結作業，而且只有在讀取時，才會將資料提供給用戶端。 換句話說，在第一次呼叫 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))之後，除非用戶端已取用所有已經可用的資料，否則該名字不會將任何資料提供給用戶端。

因為資料只會在要求時下載，所以選擇資料提取模型的用戶端必須務必及時讀取此資料。 在使用 [URL](url-monikers.md)標記的網際網路下載案例中，如果用戶端在要求更多資料之前等候太久，系結作業可能會失敗。

在資料推送模型中，此標記會驅動非同步系結作業，並在每次有新資料可用時持續通知用戶端。 用戶端可選擇是否要在系結作業期間的任何時間點讀取資料，但不論是哪一種，都要將系結作業驅動到完成。

此外，使用非同步標記時，您必須記得遵循 COM 規則來進行記憶體配置，具體如下：

-   每當 COM 介面或函式呼叫傳回緩衝區 (字串或其他) 至其用戶端時，用戶端會藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來負責釋放記憶體。
-   每當 COM 介面或函式需要其用戶端的緩衝區時，用戶端就必須使用 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 配置該緩衝區，而且被呼叫端必須釋放它。

配置傳遞給非同步標記的字串或緩衝區時，請務必遵循這些規則，並記得釋放非同步名字所傳回的記憶體。 如需完整的詳細資料，請參閱 [管理記憶體配置](the-com-library.md) 和相關主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步名字](asynchronous-monikers.md)
</dt> </dl>

 

 