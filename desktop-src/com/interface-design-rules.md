---
title: 介面設計規則
description: 本節提供介面設計規則和指導方針的簡短摘要。
ms.assetid: c43fc385-bcd6-45fc-91b2-ad9827fdb15c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d11d55a1e24c02208ebeecddd5a4f90b8b01fa4a53444e6554cfcff37165f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070808"
---
# <a name="interface-design-rules"></a>介面設計規則

本節提供介面設計規則和指導方針的簡短摘要。 其中有些規則是 COM 架構特有的，有些則是介面設計語言（MIDL）所加諸的限制。 如需 COM 介面設計的詳細資訊，請參閱 [IDL 檔案的剖析](anatomy-of-an-idl-file.md)。

根據定義，物件不是 COM 物件，除非它會執行 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面或衍生自 **iunknown** 的介面。 此外，下列規則適用于 COM 物件上所執行的所有介面：

-   它們必須有唯一的介面識別碼 (IID) 。
-   它們必須是不可變的。 一旦建立併發布之後，其定義的任何部分都不會變更。
-   所有介面方法都必須傳回 **HRESULT** 值，讓處理遠端處理的系統部分可以回報 RPC 錯誤。
-   介面方法中的所有字串參數都必須是 Unicode。
-   您的資料類型必須可以遠端處理。 如果您無法將資料類型轉換成可遠端處理的型別，就必須建立自己的封送處理和封送處理常式。 此外， **LPVOID** 或 **void \** _ 在遠端電腦上沒有任何意義。 如有必要，請使用 [_ *IUnknown* *](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的指標。

> [!Note]  
> MIDL 的目前執行不會處理函數多載或多重繼承。

 

## <a name="other-interface-design-considerations"></a>其他介面設計考慮

非常小心地使用資料指標。 若要在呼叫之進程的位址空間中重新建立資料，RPC 執行時間必須知道資料的確切大小。 例如，如果 **CHAR \*** 參數指向字元緩衝區，而不是單一字元，則無法正確地重新建立資料。 使用 MIDL 提供的語法，準確地描述您的型別定義所代表的資料結構。

針對內嵌于陣列和結構並跨進程界限傳遞的指標，初始化是不可或缺的。 未初始化的指標在傳遞至相同進程空間中的程式時可能會運作，但 proxy 和存根會假設所有指標都使用有效的位址初始化，或為 null。

當別名指標 (允許指標指向相同的記憶體) 部分時，請務必小心。 如果別名是故意的，則這些指標應該在 IDL 檔案中宣告為別名。 宣告為 nonaliased 的指標絕對不能有別名。

請注意您如何配置和釋放記憶體。 請記住，除非您使用 [ [**配置**](/windows/desktop/Midl/allocate) ] 屬性明確地告知 COM 物件 () 不要釋放跨進程調用期間所建立的資料結構，否則該結構將在呼叫完成時終結。 此外，請考慮可能會造成破壞性的資料結構配置所建立的破壞性額外負荷，現在需要封送處理和取消封送處理。

最後，定義 **HRESULT** 傳回值時請務必小心，如此一來，您就不會建立與 COM 定義的設備 ITF 程式碼衝突的錯誤碼， \_ (0x0000 和0x01FF 之間的值會保留) 或與具有相同值的其他 **HRESULT** 值發生衝突。 可能的話，請使用通用 COM 成功和失敗傳回值，並使用 [**out**](/windows/desktop/Midl/out-idl) 參數（而非 **HRESULT**）來傳回函式呼叫的特定資訊。

如需詳細資訊，請參閱下列主題：

-   [設計可遠端處理的介面](designing-remotable-interfaces.md)
-   [使用 COM 介面](using-a-com-interface.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面定義和型別程式庫](/windows/desktop/Midl/interface-definitions-and-type-libraries)
</dt> </dl>

 

 