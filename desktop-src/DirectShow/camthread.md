---
description: CAMThread 類別是用來管理工作者執行緒的抽象類別。
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: 'CAMThread 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984031"
---
# <a name="camthread-class"></a>CAMThread 類別

`CAMThread`類別是用來管理工作者執行緒的抽象類別。



| 受保護的成員變數                                 | Description                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | 執行緒的控制碼。                                                        |
| Public 成員變數                                    | Description                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | 防止其他執行緒存取執行緒的重要區段。 |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | 鎖定執行緒之間共用之資料的重要區段。                       |
| 公用方法                                             | Description                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | 函式方法。                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | 函式方法。 虛擬。                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | 在建立執行緒時呼叫 ThreadProc 方法。                      |
| [**建立**](camthread-create.md)                         | 建立執行緒。                                                          |
| [**CallWorker**](camthread-callworker.md)                 | 向執行緒發出要求的信號。                                           |
| [**關閉**](camthread-close.md)                           | 等候執行緒結束，然後釋放其資源。                   |
| [**ThreadExists**](camthread-threadexists.md)             | 查詢執行緒是否存在。                                           |
| [**GetRequest**](camthread-getrequest.md)                 | 等候下一個要求。                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | 檢查是否有要求，而不封鎖。                              |
| [**回覆**](camthread-reply.md)                           | 回復要求。                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | 抓取 CallWorker 方法所發出之事件的控制碼。           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | 捕獲最新的要求。                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | 線上程的開頭呼叫 CoInitializeEx。                             |
| 純虛擬方法                                       | Description                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | 執行緒程式。                                                            |



 

## <a name="remarks"></a>備註

這個類別提供建立背景工作執行緒、將要求傳遞至執行緒，以及等待中的執行緒結束的方法。 若要使用此類別，請執行下列動作：

-   從衍生類別 `CAMThread` ，並覆寫純虛擬方法 [**CAMThread：： ThreadProc**](camthread-threadproc.md)。 這個方法是線上程開始時呼叫的執行緒程式。
-   在您的應用程式中，建立衍生類別的實例。 建立物件並不會建立執行緒。 若要建立執行緒，請呼叫 [**CAMThread：： create**](camthread-create.md) 方法。
-   若要將要求傳送至執行緒，請呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法。 這個方法會採用 DWORD 參數，其意義是由您的類別定義。 方法會封鎖，直到執行緒回應 (請參閱以下) 。
-   在您的執行緒程式中，藉由呼叫 [**CAMThread：： GetRequest**](camthread-getrequest.md) 或 [**CAMThread：： CheckRequest**](camthread-checkrequest.md)來回應要求。 GetRequest 方法會封鎖，直到另一個執行緒呼叫 CallWorker 為止。 CheckRequest 方法為非封鎖，可讓執行緒在非同步工作時檢查是否有新的要求。
-   當執行緒收到要求時，請呼叫 [**CAMThread：： Reply**](camthread-reply.md) 來解除封鎖呼叫執行緒。 Reply 方法會採用 DWORD 參數，該參數會傳遞至呼叫的執行緒做為 CallWorker 的傳回值。

當您完成執行緒時，請呼叫 [**CAMThread：： Close**](camthread-close.md) 方法。 這個方法會等候執行緒結束，然後關閉執行緒控制碼。 您的 ThreadProc 訊息必須保證會結束，或是回應 CallWorker 要求。 「析構函數」方法也會呼叫 Close。

下列範例說明這些步驟：


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



在您的衍生類別中，您也可以定義成員函式，以驗證要 CallWorker 的參數。 下列範例顯示執行這項作業的典型方式：


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



`CAMThread`類別提供兩個重要區段作為公用成員變數。 用 `CAMThread::m_AccessLock` 來鎖定其他執行緒無法存取的執行緒。  (例如，Create 和 CallWorker 方法會保存此鎖定，以序列化執行緒上的作業。 ) 使用 [**CAMThread：： m \_ WorkerLock**](camthread-m-workerlock.md) 來鎖定執行緒之間共用的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




