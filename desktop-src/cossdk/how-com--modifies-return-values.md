---
description: COM + 如何修改傳回值
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: COM + 如何修改傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110917"
---
# <a name="how-com-modifies-return-values"></a>COM + 如何修改傳回值

COM + 絕不會變更指出失敗的 **HRESULT** 傳回值，例如 e 非 \_ 預期或 e \_ 失敗。 不過，當使用 COM + 功能的物件傳回 **HRESULT** 值，指出成功 (（例如 s \_ OK、s \_ FALSE 或 >aad-userreadusingalternativesecurityid-noerror) ）時，com + 有時會在傳回給呼叫端之前將 **hresult** 轉換成 com + 錯誤碼。

例如，當應用程式在 \_ 呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)之後傳回 S OK 時，如果物件是無法認可之交易的根，則 **HRESULT** 會轉換成內容 \_ E \_ 中止。

當 COM + 轉換 **HRESULT** 值時，它會清除所有方法的輸出參數。 傳回的參考會釋出，並將傳回的物件指標值設定為 **Null**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[找出錯誤的來源](finding-the-source-of-an-error.md)
</dt> <dt>

[解讀錯誤碼](interpreting-error-codes.md)
</dt> <dt>

[在 COM + 中處理錯誤的策略](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[疑難排解](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



